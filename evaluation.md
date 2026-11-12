# Evaluation Methodology for LoRaVoice

## 1. Objective Metrics
- **PESQ (Perceptual Evaluation of Speech Quality):** Measures overall audio quality on a scale of -0.5 to 4.5.
- **STOI (Short-Time Objective Intelligibility):** Measures the intelligibility of the speech, ranging from 0 to 1.
- **Log-Spectral Distance (LSD):** Measures the distance between the original and reconstructed mel-spectrograms.
- **Bitrate Efficiency:** Throughput (bps) required for intelligible communication.

## 2. Subjective Metrics
- **MUSHRA (MUlti-Stimulus test with Hidden Reference and Anchor):** Used for perceptual quality assessment, where listeners rank audio clips against a reference.
- **Mean Opinion Score (MOS):** Standard listener scoring (1-5) for naturalness.
- **Word Error Rate (WER):** Human transcription tests to measure practical intelligibility after codec compression.

## 3. LoRa-Specific Constraints Testing
- **Packet Loss Sensitivity:** Testing codec performance under 5%, 10%, and 20% packet loss scenarios typical in LoRa networks.
- **Latency Measurement:** Measuring end-to-end encoding/decoding time on the target hardware (Cortex-M).
- **Spreading Factor (SF) Stress Test:** Evaluating audio reconstruction degradation as the LoRa data rate decreases with increasing distance/SF.

## 4. Evaluation Workflow
1. **Dataset Generation:** Take a standard test set (e.g., TIMIT).
2. **Simulation:** Feed through the LoRaVoice encoder/decoder simulator.
3. **Impairment Simulation:** Inject network-specific impairments (jitter, packet loss, latency).
4. **Performance Scoring:** Aggregate objective and subjective metrics.
