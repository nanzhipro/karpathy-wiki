---
title: GPU MODE IRL 2024 — Karpathy on llm.c
type: source-summary
created: 2026-04-17
updated: 2026-04-17
sources: [gpu-mode-irl-2024-keynotes/transcript.md]
tags: [llm-c, cuda, training, systems, pytorch, karpathy]
---

# GPU MODE IRL 2024 — Karpathy on llm.c

**Speaker:** [[andrej-karpathy|Andrej Karpathy]] (one of six keynote speakers)
**Venue:** GPU MODE IRL 2024, hosted at Accel's office (September 2024; video published October 2, 2024)
**Original source:** `raw/youtube-transcript/gpu-mode/gpu-mode-irl-2024-keynotes/transcript.md`
**Karpathy segment:** ~30:50–54:06 (~23 min of 108 min total)
**Format:** technical talk + mini war-story

> **Note:** Only Karpathy's segment is summarized here. Other speakers at the event: Tri Dao (FlashAttention-3), Supriya Rao (torchao), Lily Liu (vLLM), Tim Dettmers (open-source strategy & bitsandbytes), Wen-mei Hwu (GPU architecture history). Their talks are orthogonal to this wiki's focus.

## Thesis

[[llm-c]] is Karpathy's from-scratch implementation of GPT-2 training in pure C + a pinch of C++, plus hand-written CUDA. The talk is both a project retrospective and an argument: if **PyTorch + torch.compile is the GCC of Software 2.0, llm.c is the assembly**. He predicts that as LLMs become capable compilers themselves, bespoke low-level code may become the normal output — and llm.c exists partly to be example code put in LLM context to make that possible.

## Key Claims

1. **The project began as anger at `torch.compile`.** Karpathy was trying to add a video to [[zero-to-hero|Zero to Hero]]: teach GPT-2 training, hacking on [[nanogpt]]. Training worked; eval and inference both died with unrelated `torch.compile` errors. Two hours of grief, a visit to the PyTorch forum looking for `ptrblck`, and no fix. The response: *"I'll just write the whole thing myself."* *(origin story)*
2. **PyTorch gives you a lot; giving it up is instructive.** Enumerated explicitly: n-dimensional arrays, autograd, device management, dtype conversions, `torch.compile`, and distributed training — each one a headline feature you have to rebuild by hand in C. The project is a deliberate tour of what frameworks do for you. *(pedagogical framing)*
3. **Layer-by-layer port is tractable.** Keep the PyTorch version as a reference; for each layer (e.g. LayerNorm), (a) write the forward pass manually in PyTorch (because PyTorch calls into CUDA for LayerNorm and doesn't expose the actual forward), (b) write the backward by hand ("take out your pen and paper"), (c) verify numerical equivalence, (d) port to C as `float*` arrays with pointer arithmetic. *"No tensor abstraction — just float arrays and operations on float arrays. Why should it be more complicated?"* *(how-to, single-source)*
4. **All memory pre-planned at startup.** Every tensor's size is computed once; a single blob is allocated at startup and never grown. Result: no OOMs mid-training, no allocator surprises, fully deterministic memory profile. *"In principle this could run on a von Neumann probe."* *(design principle)*
5. **~2000 lines of C, no dependencies, compiles and runs instantly.** The baseline C version trains GPT-2 end to end and matches the PyTorch reference numerically. Written largely on vacation in the Maldives at 1 a.m., jetlagged. *(anecdote)*
6. **Port to CUDA is versioned per kernel.** Each layer ships as `kernel_1.cu`, `kernel_2.cu`, ... through increasingly sophisticated optimizations. First kernel is usually trivial (parallelize over batch × time). Later kernels use warp-specialization, shared memory, cache-streaming hints. Learning CUDA was harder than Karpathy expected — PMPP is good but beginner-oriented, and Simon Boehm's GEMM blog post is "way better than anything we deserve." *(evaluation of the learning materials)*
7. **An "Avengers" team assembled from the internet.** Core devs Eric, Arun, Alex joined; 60+ contributors total. Lambda sponsored compute. *"One of my favorite things that can happen with an open-source MIT repo — people just come from the internet and help contribute."* *(community pattern)*
8. **Optimizations that worked (and one that didn't).** (a) `cuBLAS` for matmuls; (b) cuDNN FlashAttention; (c) mixed precision (fp32/bf16); (d) kernel fusions; (e) selective recompute in the backward; (f) a `Packed128` data structure that *forces* the NVCC compiler to emit 128-bit load/store instructions (it otherwise refuses); (g) **CUDA streams were deleted** — `Ctrl-F` for "stream" and nuke it; the race conditions weren't worth the overlap. Stochastic rounding. Full determinism. *(concrete engineering)*
9. **Result: GPT-2 1.6B reproduced on a single H100 node in ~24 hours for ~$600.** Heaviest dependency is cuDNN, which is optional; no Python, no conda, no pip. Compiles and runs in seconds. At the time of the accompanying blog post, llm.c used **30% less memory and ran 20% faster** than PyTorch for GPT-2 training specifically. *(headline result)*
10. **LLMs will become compilers; llm.c is the demo.** Karpathy's forward-looking claim: if PyTorch + torch.compile is like GCC for Software 2.0, llm.c is writing assembly. Doing llm.c-level work cost a team several months; an LLM that becomes good at coding can do the same for *any* custom app. "The `llm.c` repo might be useful because... few-shot learning would be very helpful for the LLM to basically give it example code." *(single-source forecast, connects to [[software-3-0]])*

## Structure of the Talk

1. Origin: nanoGPT + torch.compile hell → "I'll write it in C."
2. What PyTorch gives you (that you're about to lose).
3. Layer-by-layer port: PyTorch reference → explicit forward/backward → float-array C.
4. Pre-planned memory, no dependencies, Maldives anecdote.
5. Port to CUDA: versioned kernels, learning materials, Simon Boehm shout-out.
6. Team assembles: contributors, Lambda compute, optimization list.
7. Multi-GPU (NCCL, ZeRO-1 sharded optimizer state), multi-node.
8. Result: GPT-2 1.6B, 24h, $600, 30% less memory, 20% faster than PyTorch.
9. llm.c as "assembly" of Software 2.0 — and as few-shot example code for future coding LLMs.

## Notable Quotes

> "If PyTorch is like GCC for Software 2.0, llm.c is like writing assembly."

> "I was in denial. Then I entered the stage of anger. So I was like — okay, you know what, I'm just going to write the whole thing."

> "Everything is just float arrays. No tensor abstraction. Why should it be more complicated than that?"

> "All the memory is just allocated in a single blob. If you start stepping, there's no way you're going to OOM later — it's all pre-planned, fully deterministic. It can train GPT-2. It can run on a potato. This would be a great candidate to run on a von Neumann probe."

> "I just `Ctrl-F`'d for all mentions of `stream` and nuked it from orbit. Made everything single-threaded. Too much complexity for not enough gain."

> "The llm.c repo might be useful because in the early stages of these LLMs and their intelligence, they might not be able to write this code from scratch. But you're a lot more likely to get it if you put llm.c in the context."

## Named Entities & References

- [[andrej-karpathy|Andrej Karpathy]] — speaker
- [[llm-c]] — the project; ~3000 lines of C + CUDA, MIT-licensed
- [[nanogpt]] — the PyTorch project llm.c grew out of
- [[zero-to-hero]] — the YouTube series for which Karpathy was recording the video that triggered the anger
- [[pytorch]] — the framework being both depended on and shed
- Simon Boehm — blog post author, recommended as the best CUDA GEMM reference
- PMPP (Wen-mei Hwu) — CUDA textbook, "quite good but beginner-level"
- CUDA C++ Programming Guide — "not exactly readable"
- Lambda — compute sponsor
- Eric Arun, Arun, Alex — core contributors
- `ptrblck` — PyTorch-forum user Karpathy was hunting for help from
- AMD fork, C++ fork of llm.c — notable community forks

## Concepts Introduced / Reinforced

- [[llm-c]] — project entity
- [[software-3-0]] — reinforced: LLMs as compilers for custom code
- [[ramps-to-knowledge]] — llm.c as a hand-crafted pedagogical ramp
- [[nanogpt]], [[nanochat]], [[micrograd]] — siblings in Karpathy's ramp series

## Open Questions

- Is the "LLM writes llm.c for your app" prediction tracking? (As of 2025–2026 source dates, coding LLMs write PyTorch fluently but aren't yet producing fused CUDA kernels reliably.)
- What's the actual maintenance burden on llm.c post-2024? Karpathy says Llama 3 and fp8 support are "coming"; needs verification against the current repo state.
- The Packed128 finding (compiler refusing 128-bit load/store) — has anyone upstreamed that into NVCC's optimizer?

## My Reading (commentary)

Two things make this talk distinctive in Karpathy's corpus. First, it's the clearest articulation of the **Software 1.0 / 2.0 / 3.0 stack as an execution hierarchy**: PyTorch code is the high-level language, torch.compile is the compiler, hand-written CUDA is the assembly. That hierarchy shows up in [[software-is-changing-again]] as a metaphor; here it's the literal project structure. Second, the prediction that **LLM-written code replaces the PyTorch abstraction for custom apps** is Karpathy's most concrete commitment about where the stack is going — and the repo itself is positioned as the training-data sacrifice on the altar of that future.
