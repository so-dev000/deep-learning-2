# Deep Learning from Scratch 2 - Project Overview

## Project Purpose
This is the support repository for the book "ゼロから作るDeep Learning ❷ ―自然言語処理編" (Deep Learning from Scratch 2 - Natural Language Processing Edition) published by O'Reilly Japan.

The project contains source code examples and implementations for the book chapters, focusing on natural language processing using deep learning techniques built from scratch without high-level frameworks.

## Current Project Structure

### Jupyter Notebooks (Main Content)
- **ch01.ipynb**: Neural networks basics (spiral dataset, two-layer networks, training loops)
- **ch02.ipynb**: Word similarity and co-occurrence matrix, PPMI, SVD  
- **ch03.ipynb**: CBOW and Skip-gram models
- **ch04.ipynb**: Word2Vec with negative sampling
- **ch05.ipynb**: Simple RNN language models
- **ch06.ipynb**: Gated RNN, LSTM, gradient clipping
- **ch07.ipynb**: Sequence-to-sequence models, text generation
- **ch08.ipynb**: Attention mechanism

Each notebook contains all Python files from the corresponding chapter as separate code cells, with proper imports fixed for the new structure.

### Support Directories
- **common/**: Shared utilities and core implementations
  - `layers.py`: Neural network layer implementations (MatMul, Affine, Softmax, etc.)
  - `optimizer.py`: Optimization algorithms (SGD, Adam, etc.)
  - `trainer.py`: Training utilities
  - `config.py`: Configuration settings (GPU mode toggle)
  - `np.py`: NumPy/CuPy abstraction layer
  - `util.py`: Common utility functions
- **dataset/**: Dataset utilities and loading functions
  - `spiral.py`: Spiral dataset for classification
  - `ptb.py`: Penn Treebank dataset
  - `sequence.py`: Sequence data utilities

### Model Files (Pickled)
- **cbow_params.pkl**: Trained CBOW model parameters (from ch04)
- **Rnnlm.pkl**: Trained RNN language model (from ch06)
- **AttentionSeq2seq.pkl**: Trained attention-based seq2seq model (from ch08)

### Other Files
- **LICENSE.md**: MIT License
- **README.md**: Japanese documentation with setup instructions

## Important Changes Made
1. **Converted to Jupyter notebooks**: All chapter Python files are now contained in single notebooks per chapter
2. **Removed chapter directories**: The original ch01-ch08 directories have been removed
3. **Fixed imports**: All `sys.path.append('..')` statements removed and local imports properly handled
4. **Centralized models**: .pkl files moved to root directory for easy access

## Book Context
This is an educational codebase designed to teach deep learning concepts by implementing them from first principles, with a focus on natural language processing applications. The Jupyter notebook format makes it easier to run and experiment with the code interactively.