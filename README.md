# Official Code Repository: Understanding Generalization of Quantum Adversarial Machine Learning via Stability

This repository contains the official code implementation for the paper **"Understanding generalization of quantum adversarial machine learning via stability"**.

This project investigates the algorithmic stability and generalization capabilities of Data Re-uploading Quantum Neural Networks (DReQNN) under adversarial attacks of varying intensities. Through empirical research, we reveal how different topological arrangements of quantum circuits (the ratio of parameterized layers to encoding layers) impact the model's robustness against adversarial perturbations.

## Repository Structure

The codebase is systematically organized based on the datasets and experimental variables:

```text
.
│  Data_process.ipynb          # Data preprocessing (dimensionality reduction/feature extraction) pipeline
│  Quantum_DReQNN.ipynb        # Base DReQNN architecture and adversarial attack simulation environment
│  Special_layers.ipynb        # Ablation study on specific encoding layer structures
│
├─PAC/                         # Cache directory for preprocessed features
│      processed_fmnist.pt     # PyTorch tensor for Fashion-MNIST
│      processed_kmnist.pt     # PyTorch tensor for KMNIST
│
├─Fashion-MNIST/               # Stability evaluation for Fashion-MNIST
│  ├─Various_epsilon/          # [Exp 1] Generalization bounds: Robustness under various attack strengths (eps)
│  │  │  main.ipynb            
│  │  └─Results/               # Outputs (eps=0.06 ~ 0.3)
│  │
│  └─Various_layers/           # [Exp 2] Structural stability: Impact of varying Encoding layers (Enc)
│      │  main.ipynb           
│      └─Results/              # Outputs (Fixed PQC=15, varying Enc layers)
│
└─KMNIST/                      # Stability evaluation for KMNIST (same structure as above)
   ├─Various_epsilon/          
   └─Various_layers/
