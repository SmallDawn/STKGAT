# STKGAT: Spatial-Temporal Key Node Graph Attention Network with Positional Encoding

**Deployment and implementation details for the STKGAT model.**

## Status: Coming Soon

## Implementation Details & Deployment Configuration

The model and experiments described in the paper were implemented and conducted with the following specifications:

### Environment
- **Framework**: PyTorch 2.3.1
- **GPU**: NVIDIA RTX A6000

### Training Configuration
- **Optimizer**: Adam
- **Initial Learning Rate**: 0.001
- **Batch Size**: 32
- **Weight Decay**: $3 \times 10^{-4}$
- **Learning Rate Schedule**: Reduced by a factor of 0.3 every 20 epochs.
- **Early Stopping**: Patience of 10 epochs.

### Model Architecture
- **Embedding Dimension**: 64
- **Attention Heads**: 8
- **Encoder Layers**: 3
- **Decoder Layers**: 3

### Data Split
- **Training**: 70% (chronological)
- **Validation**: 10%
- **Testing**: 20%

### Hyperparameter Tuning
Key hyperparameters were tuned over 5 independent runs per configuration. The main parameters tuned were:
- Number of key nodes ($N_K$)
- Historical window size ($\Delta t$)
- Architecture parameters
