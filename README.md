# DeepSets vs GNN Comparison

This project compares **DeepSets** and several **Graph Neural Networks (GNNs)** (GCN, GraphSAGE, GIN, GAT) on synthetic datasets.  
It includes dataset generation, training, hyperparameter grid search, and testing

---

## Installation

Clone the repo and install dependencies:

The code uses PyTorch and PyTorch Geometric.
If you have a CUDA-capable GPU, install the CUDA version of PyTorch first:

```bash
# Example: PyTorch 2.2.2 with CUDA 12.1
pip install torch==2.2.2+cu121 torchvision==0.17.2+cu121 torchaudio==2.2.2 --extra-index-url https://download.pytorch.org/whl/cu121
```

```bash
pip install -r requirements.txt
```

## Running the Project

The main entry point is main.py:
```bash
python main.py
```

### What happens:

- Synthetic point set data is generated.
- Data is converted into graphs.
- Train/val/test splits are created.
- A grid search runs for DeepSets and each GNN model.
- The best models are saved (.pt files).
- Best hyperparameters are saved as JSON.
- Models are tested on the test set.

### Results:
The testing function automatically saves evaluation outputs to the results/ directory.
⚠️ Note: the save path is currently hardcoded inside the code. If you want results in a different location, update the path in testing.py.
