## Open Source Contributions

Merged in three repositories of the
[vllm-project](https://github.com/vllm-project) organization.

### [vllm](https://github.com/vllm-project/vllm) : the inference engine

- [**hadacore_transform: respect inplace parameter**](https://github.com/vllm-project/vllm/pull/43462) :
  the kernel wrote its output into the input tensor, ignoring the
  `inplace` parameter; under torch.compile, QuIP models produced garbage outputs

### [llm-compressor](https://github.com/vllm-project/llm-compressor) : quantization toolkit for LLM deployment

*Approved and merged by the projects' maintainers.*

- [**iMatrix weighted MSE observer and IMatrixGatherer**](https://github.com/vllm-project/llm-compressor/pull/2473) :
  importance-weighted (E[x²]) range selection, no full Hessian
- [**Norm calibration context for unit-offset RMSNorm**](https://github.com/vllm-project/llm-compressor/pull/2500) :
  fixes garbage AWQ output on Gemma
- [**MoE calibration module for GlmMoeDsa (GLM-5)**](https://github.com/vllm-project/llm-compressor/pull/2434) :
  unpacks GLM-5's packed 3D expert weights
- [**Topological ordering in FX graph cleanup**](https://github.com/vllm-project/llm-compressor/pull/2426) :
  fixes `erase_node` crash on Granite4 GPTQ
- [**Packed weight handling in granite4 to_3d_expert**](https://github.com/vllm-project/llm-compressor/pull/2425) :
  W4A16 support
- [**SmoothQuant regex fix for q_a_proj**](https://github.com/vllm-project/llm-compressor/pull/2421) :
  DeepSeek and GLM-5
- [**SmoothQuant mapping for GLM-5**](https://github.com/vllm-project/llm-compressor/pull/2419)
- [**AWQ mapping for GLM-5**](https://github.com/vllm-project/llm-compressor/pull/2418)
- [**MR-GPTQ example**](https://github.com/vllm-project/llm-compressor/pull/2751) :
  QuIP + GPTQ + NVFP4A16

### [compressed-tensors](https://github.com/vllm-project/compressed-tensors) : safetensors extension for sparse and quantized tensors

*Approved and merged by the projects' maintainers.*

- [**N-dimensional tensor support in pack/unpack_int32**](https://github.com/vllm-project/compressed-tensors/pull/609) :
  fixes 3D MoE expert weight packing
- [**cast_to_fp4 per-rank torch.compile recompilation fix**](https://github.com/vllm-project/compressed-tensors/pull/741) :
  removes a Dynamo recompile storm on NVFP4 MoE generation

## GPU Kernels

- **[gemm-ladder](https://github.com/Yatimai/gemm-ladder)** : an fp16 GEMM
  built step by step on a T4, from NVIDIA's tensor-core sample, adapted
  (0.62x), to 1.05x the judge's fastest cuBLASLt configuration, with the
  tools and raw outputs in the repository.

## Applied AI Systems

- **[finsight](https://github.com/Yatimai/finsight)** : visual RAG
  over 10 French annual reports (ColQwen2.5 + Qdrant).
  5,982 pages indexed, 92% Recall@10, 84% strict answer accuracy
  (LLM-judge on non-circular ground truth), 92% citation faithfulness.
  Async FastAPI with SSE streaming, React frontend, 184 tests, CI.
- **[reasonforge](https://github.com/Yatimai/reasonforge)** :
  iterative self-improvement for Text-to-SQL on Ministral-8B.
  Spider dev: 60.1% base, 68.8% SFT, 78.0% looped with k=16
  self-consistency (vLLM + LoRA + H200).
- **[ai-watch](https://github.com/Yatimai/ai-watch)** : autonomous AI
  news agent on LangGraph. Daily briefings in production since
  February 2026 via GitHub Actions.
