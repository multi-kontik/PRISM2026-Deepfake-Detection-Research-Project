# PRISM2026-Deepfake-Detection-Research-Project

# 1. Compression Threshold for Temporal Deepfake Detection
This research investigates the "Critical Decay Point" of video compression, where the academic advantage of temporal analysis over spatial analysis in deepfake detection fails due to real-world data degradation.

# 2. 🔬 Research Overview
Topic: Compression threshold for temporal model efficacy in deepfake detection.

Problem: While temporal models (e.g., 3D-CNNs, LSTMs) typically outperform spatial ones in high-quality laboratory settings, aggressive social media compression (H.264/H.265) acts as a temporal low-pass filter, destroying the high-frequency signals these models rely on.

Hypothesis: There exists a point of critical decay beyond which temporal analysis no longer outperforms robust spatial models configured on identical training data.

# 3. 🛠️ Methodology
The project utilizes DeepfakeBench, a unified open-source benchmarking framework, to isolate compression as the sole variable.

1. Data Preparation

Source: FaceForensics++ dataset.

Processing: Videos are re-encoded at controlled compression levels using FFmpeg with varying Constant Rate Factor (CRF) levels.

Controls: Framerate and resolution are held constant to ensure compression is the only variable.

2. Evaluation Pipeline

Detectors: Both spatial and temporal detectors are trained and evaluated under identical conditions.

Baseline: Standard C23 (High Quality) and C40 (Low Quality) levels built into FaceForensics++.

Tools: Python-based analysis using Matplotlib and Seaborn for visualization.

# 4. 📊 Expected Outcomes
Identify the Critical Decay Point: Pinpointing the specific bitrate/CRF where temporal models lose their forensic advantage.

Bridge the "Generalization Gap": Explaining why models with 95%+ laboratory accuracy experience a 10–15% performance drop in real-world scenarios.

Optimization: Proposing an ideal weight for spatial vs. temporal analysis based on the detected compression level to maximize system robustness.

# 📚 Key References
DeepfakeBench: Yan et al. (2023) .

AltFreezing: Wang et al. (2023) .

Temporal Coherence: Amin et al. (2024) .

Quantization Noise: Nguyen & Vo (2025).
