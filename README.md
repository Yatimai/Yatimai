I build and optimize LLM systems. Active open-source contributor to the vLLM ecosystem (llm-compressor, compressed-tensors). I also develop production-grade LLM applications in RAG, fine-tuning, and autonomous agents.

## Open Source Contributions

**[vllm-project/llm-compressor](https://github.com/vllm-project/llm-compressor)** — Quantization toolkit for LLM deployment with vLLM

- [Add iMatrix weighted MSE observer and IMatrixGatherer](https://github.com/vllm-project/llm-compressor/pull/2473) — importance-weighted quantization, improves PPL across RTN/GPTQ/AWQ
- [Add norm calibration context for unit-offset RMSNorm (Gemma/Qwen3Next)](https://github.com/vllm-project/llm-compressor/pull/2500) — fixes AWQ/SmoothQuant on Gemma models
- [Add MoE calibration module for GlmMoeDsa (GLM-5)](https://github.com/vllm-project/llm-compressor/pull/2434) — packed 3D tensor handling for MoE architectures
- [Fix topological ordering in FX graph cleanup](https://github.com/vllm-project/llm-compressor/pull/2426) — erase_node crash fix for Granite4 GPTQ
- [Handle packed weights in granite4 to_3d_expert (W4A16)](https://github.com/vllm-project/llm-compressor/pull/2425)
- [Fix SmoothQuant regex for DeepSeek/GLM-5](https://github.com/vllm-project/llm-compressor/pull/2421)
- [Add SmoothQuant mapping for GLM-5](https://github.com/vllm-project/llm-compressor/pull/2419)
- [Add AWQ mapping for GLM-5](https://github.com/vllm-project/llm-compressor/pull/2418)

**[vllm-project/compressed-tensors](https://github.com/vllm-project/compressed-tensors)** — Safetensors extension for sparse and quantized tensor storage

- [Support N-dimensional tensors in pack/unpack_int32](https://github.com/vllm-project/compressed-tensors/pull/609) — fixes 3D MoE expert weight packing

## Projects

- **[finsight](https://github.com/Yatimai/finsight)** — Visual RAG for French financial documents using ColQwen2.5 + Qdrant + Claude Sonnet/Opus. Indexed 10 annual reports (~5,982 pages). 90% Recall@10, 100% citation accuracy. Async FastAPI backend with SSE streaming + background adversarial verification, React + base-ui frontend. 183 tests, CI/CD.
- **[reasonforge](https://github.com/Yatimai/reasonforge)** — Iterative LLM fine-tuning on Text-to-SQL using STaR (Self-Taught Reasoner). Ministral-8B: 60.1% baseline → 68.8% SFT → 78.0% after 3 STaR iterations on Spider dev set.
- **[ai-watch](https://github.com/Yatimai/ai-watch)** — Autonomous AI news agent via LangGraph + Claude. Daily briefings on quantization and LLM research topics.
