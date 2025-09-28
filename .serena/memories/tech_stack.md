# Technology Stack

## Core Dependencies
- **Python 3.x**: Required runtime (Python 3 series)
- **NumPy**: Core numerical computing library
- **Matplotlib**: Plotting and visualization
- **Jupyter**: Interactive notebook environment for running code examples

## Optional Dependencies
- **SciPy**: Optional scientific computing library
- **CuPy**: Optional GPU acceleration (CUDA support)
- **scikit-learn**: Used in some examples for utilities like randomized SVD

## Development Environment
- **Jupyter Notebook/Lab**: Primary interface for running chapter code
- All chapter code is now organized in .ipynb notebook files
- Interactive execution and visualization capabilities

## GPU Support
The project includes GPU acceleration support through CuPy:
- Controlled by `common/config.py` with `GPU = False` by default
- When enabled, `common/np.py` switches from NumPy to CuPy
- Memory pool optimization for GPU usage

## Architecture
- Pure Python implementation without high-level ML frameworks
- Custom neural network layers built from scratch
- Modular design with shared utilities in `common/`
- Educational focus on understanding fundamentals
- Jupyter notebook format for interactive learning

## File Formats
- **Python (.py)**: Utility modules in `common/` and `dataset/`
- **Jupyter Notebooks (.ipynb)**: Chapter code examples (ch01-ch08)
- **Pickle (.pkl)**: Trained model parameters

## No Package Management
- No requirements.txt, setup.py, or pyproject.toml found
- Dependencies are minimal and standard
- Manual dependency management expected
- Jupyter must be installed separately