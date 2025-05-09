# Qwen2.5 14B Job Parsing Model

This repository contains code and notebooks for fine-tuning and using the Qwen2.5 14B model for job description parsing tasks. The project uses the Unsloth framework for efficient fine-tuning and inference.

## Project Structure

```
.
├── notebooks/
│   ├── Dataset_preparation.ipynb    # Data preprocessing and preparation
│   ├── finetuning.ipynb            # Model fine-tuning process
│   └── inference.ipynb             # Model inference and evaluation
```

## Requirements

- Python 3.x
- CUDA-compatible GPU (recommended: Tesla T4 or better)
- Required Python packages:
  - unsloth
  - bitsandbytes
  - accelerate
  - xformers==0.0.29.post3
  - peft
  - trl
  - triton
  - cut_cross_entropy
  - unsloth_zoo
  - sentencepiece
  - protobuf
  - datasets
  - huggingface_hub
  - hf_transfer

## Installation

1. Clone this repository:
```bash
git clone [repository-url]
cd finetuning_Qwen2.5_14B_job_parsing
```

2. Install the required packages:
```bash
pip install --no-deps bitsandbytes accelerate xformers==0.0.29.post3 peft trl triton cut_cross_entropy unsloth_zoo
pip install sentencepiece protobuf datasets huggingface_hub hf_transfer
pip install --no-deps unsloth
```

## Usage

### 1. Data Preparation

Open and run the `Dataset_preparation.ipynb` notebook to:
- Process and clean job descriptions
- Prepare the dataset for fine-tuning
- Generate training and validation splits

### 2. Fine-tuning

The `finetuning.ipynb` notebook contains the complete fine-tuning process:
- Model initialization
- Training configuration
- Fine-tuning execution
- Model checkpointing

### 3. Inference

Use the `inference.ipynb` notebook to:
- Load the fine-tuned model
- Run inference on new job descriptions
- Evaluate model performance

## Hardware Requirements

- GPU: NVIDIA GPU with at least 16GB VRAM (Tesla T4 or better recommended)
- RAM: Minimum 32GB recommended
- Storage: At least 100GB free space for model weights and datasets

## Notes

- The project uses the Unsloth framework for optimized training and inference
- Fine-tuning is performed using LoRA (Low-Rank Adaptation) for efficient parameter updates
- The model is based on Qwen2.5 14B architecture

## Acknowledgments

- Qwen team for the base model
- Unsloth team for the optimization framework
