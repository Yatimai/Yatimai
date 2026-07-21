## Open Source Contributions

**[vllm-project/llm-compressor](https://github.com/vllm-project/llm-compressor)** : Quantization toolkit for LLM deployment with vLLM

- [Add iMatrix weighted MSE observer and IMatrixGatherer](https://github.com/vllm-project/llm-compressor/pull/2473) : importance-weighted quantization, improves PPL across RTN/GPTQ/AWQ
- [Add norm calibration context for unit-offset RMSNorm (Gemma/Qwen3Next)](https://github.com/vllm-project/llm-compressor/pull/2500) : fixes AWQ/SmoothQuant on Gemma models
- [Add MoE calibration module for GlmMoeDsa (GLM-5)](https://github.com/vllm-project/llm-compressor/pull/2434) : packed 3D tensor handling for MoE architectures
- [Fix topological ordering in FX graph cleanup](https://github.com/vllm-project/llm-compressor/pull/2426) : erase_node crash fix for Granite4 GPTQ
- [Handle packed weights in granite4 to_3d_expert (W4A16)](https://github.com/vllm-project/llm-compressor/pull/2425)
- [Fix SmoothQuant regex for DeepSeek/GLM-5](https://github.com/vllm-project/llm-compressor/pull/2421)
- [Add SmoothQuant mapping for GLM-5](https://github.com/vllm-project/llm-compressor/pull/2419)
- [Add AWQ mapping for GLM-5](https://github.com/vllm-project/llm-compressor/pull/2418)

**[vllm-project/compressed-tensors](https://github.com/vllm-project/compressed-tensors)** : Safetensors extension for sparse and quantized tensor storage

- [Support N-dimensional tensors in pack/unpack_int32](https://github.com/vllm-project/compressed-tensors/pull/609) : fixes 3D MoE expert weight packing

## GPU Kernels (FP4 / Blackwell)

NVFP4/MXFP4 kernel optimization on B200 (SOL-ExecBench, NVIDIA): median SOL 0.89 across 12 NVFP4 problems, benchmark of 235 real-model kernels scored by distance to the hardware roofline. Techniques: fused FP4 quantization, vectorized memory access, warp-level reduction, and a hand-written Blackwell 4-bit matmul (CUDA, tcgen05, async copies) where it mattered.
