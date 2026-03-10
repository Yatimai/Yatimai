
# Hi, I'm Gilles 

ML Engineer specializing in LLM quantization and inference optimization. Active open-source contributor to the vLLM ecosystem.

## Open Source Contributions

**[vllm-project/llm-compressor](https://github.com/vllm-project/llm-compressor)** — Quantization toolkit for LLM deployment with vLLM
- [[RFC] iMatrix weighted MSE observer for weight quantization](https://github.com/vllm-project/llm-compressor/issues/2456) — 21% perplexity reduction at W3, 2.5× GSM8K accuracy improvement
- [Add MoE calibration module for GlmMoeDsa (GLM-5)](https://github.com/vllm-project/llm-compressor/pull/2434) — Packed 3D tensor handling for MoE architectures
- [Fix topological ordering in FX graph cleanup](https://github.com/vllm-project/llm-compressor/pull/2426) — erase_node crash fix for Granite4 GPTQ
- [Handle packed weights in granite4 to_3d_expert (W4A16)](https://github.com/vllm-project/llm-compressor/pull/2425)
- [Fix SmoothQuant regex for DeepSeek/GLM-5](https://github.com/vllm-project/llm-compressor/pull/2421)
- [Add SmoothQuant mapping for GLM-5](https://github.com/vllm-project/llm-compressor/pull/2419)
- [Add AWQ mapping for GLM-5](https://github.com/vllm-project/llm-compressor/pull/2418)

**[vllm-project/compressed-tensors](https://github.com/vllm-project/compressed-tensors)**
- [Support N-dimensional tensors in pack/unpack_int32](https://github.com/vllm-project/compressed-tensors/pull/609)

**[axolotl-ai-cloud/axolotl](https://github.com/axolotl-ai-cloud/axolotl)** — LLM fine-tuning framework
- [Fix batch_size with tensor parallelism](https://github.com/axolotl-ai-cloud/axolotl/pull/3462)
- [Fix total_num_steps with context parallelism](https://github.com/axolotl-ai-cloud/axolotl/pull/3444)

## Projects

- **[ai-watch](https://github.com/Yatimai/ai-watch)** — Autonomous AI news agent via LangGraph + Claude
- **[reasonforge](https://github.com/Yatimai/reasonforge)** — Iterative LLM fine-tuning on Text-to-SQL using STaR
- **[finsight](https://github.com/Yatimai/finsight)** — Visual RAG for financial document analysis with ColQwen2, Qdrant, Claude
