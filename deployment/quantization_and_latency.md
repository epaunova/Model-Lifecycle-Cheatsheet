# 🚀 Quantization & Latency Optimization

Optimizing LLMs for production often requires trade-offs in model size and inference speed.

## Techniques

- **INT8 Quantization**: Reduces model size 4x with minimal loss
- **GPTQ / AWQ**: Advanced quantization algorithms
- **ONNX Export**: Enables serving via Triton or TensorRT

## Inference Tips

- Use `torch.compile()` (PyTorch 2.0) for faster throughput
- Combine LoRA + quantization for edge devices