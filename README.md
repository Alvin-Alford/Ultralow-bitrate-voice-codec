# LoRaVoice

LoRaVoice is an ultra-low-bitrate neural audio codec designed specifically for bandwidth-constrained IoT applications over LoRa networks. By leveraging Residual Vector Quantization (RVQ) and a lightweight generative vocoder, it delivers natural, intelligible speech at 500–1200 bps, optimized for resource-constrained edge devices (ARM Cortex-M / RISC-V).

## Key Features
- **Ultra-Low Bitrate:** Target range of 500 bps to 1.2 kbps, suitable for LoRa bandwidth limits.
- **Natural Speech Quality:** Uses generative decoding to maintain human-like speech characteristics and intelligibility.
- **Edge Optimized:** Lightweight encoder architecture designed for deployment on low-power microcontrollers via TFLite Micro or CMSIS-NN.
- **Packet Loss Resilient:** Designed to handle intermittent connectivity typical in long-range wireless networks.

## Project Documentation
- [Architecture Overview](architecture.md): Detailed design of the encoder, transmission format, and generative decoder.
- [Training Plan](training_plan.md): Strategy for model training, quantization, and edge optimization.
- [Evaluation Methodology](evaluation.md): Objective (PESQ, STOI) and subjective (MUSHRA, MOS) testing plans.

## Getting Started
*(Coming soon: Dataset preparation scripts, PyTorch training pipeline, and C++ inference code for microcontrollers.)*

## License
MIT License
