# CSI-Aware GNN-Based Channel Decoder for 5G NR LDPC Codes

A Graph Neural Network (GNN) decoder for 5G NR LDPC codes that uses channel state information (CSI) and outperforms a standard Belief Propagation (BP) baseline. Team project at GITAM (3 members, equal contribution), Aug 2025 – Apr 2026.

## Overview
Traditional BP decoding uses fixed message-passing rules on the code's Tanner graph. This project replaces those rules with **trainable MLPs** that operate on the same graph structure, and feeds in CSI through SNR-aware features so the decoder adapts to channel conditions.

## Key Features
- CSI-aware GNN decoder for 5G NR LDPC codes
- Trainable MLPs replacing BP update rules on the Tanner graph
- Synthetic data for **AWGN** and **Rayleigh fading** channels
- Configurations with **10, 15 and 20 GNN layers**
- Evaluated over a **0–5 dB Eb/No** range
- Automated CSV logging and BER-vs-Eb/No plots

## Results
The GNN decoder achieved an **8–43% improvement in Bit Error Rate (BER)** over the BP baseline.

<!-- Add your BER vs Eb/No plot here: ![BER plot](results/ber_plot.png) -->
<!-- Optional: add a small table of BER values for BP vs GNN (10/15/20 layers) at a few Eb/No points -->

## Tech Stack
Python · TensorFlow / Keras · NVIDIA Sionna · NumPy · Pandas · Matplotlib · Google Colab (NVIDIA V100/A100 GPUs)

## Repository Structure
```
├── notebooks/    # Colab notebooks for training and evaluation
├── src/          # Model, training and evaluation code
├── results/      # CSV logs and BER plots
├── requirements.txt
└── README.md
```

## How to Run
1. Open the notebook in Google Colab and select a GPU runtime.
2. Install dependencies: `pip install tensorflow sionna pandas matplotlib`
3. Run the training cells, then the evaluation cells to generate the BER plots.

<!-- Fill in: exact notebook names and any config options -->

## Team
Team of 3 members with equal contribution. <!-- Add teammate names and GitHub links if they agree -->

## Author
Yashwanth Sarika · [LinkedIn](https://linkedin.com/in/yashwanthsarika)
