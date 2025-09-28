# Suggested Development Commands

## Running Code
The project now uses Jupyter notebooks instead of separate Python files:

```bash
# Start Jupyter notebook server
jupyter notebook

# Or use JupyterLab
jupyter lab

# Run specific notebook
jupyter notebook ch01.ipynb
```

## Working with Notebooks
```bash
# Convert notebook to Python script (if needed)
jupyter nbconvert --to script ch01.ipynb

# Execute notebook from command line
jupyter nbconvert --execute --to notebook ch01.ipynb
```

## System Commands (macOS/Darwin)
- `ls` - List directory contents
- `cd` - Change directory  
- `find` - Search for files
- `grep` - Search within files
- `git` - Version control operations

## Python Environment
```bash
# Activate virtual environment (if using)
source .venv/bin/activate

# Install dependencies
pip install jupyter numpy matplotlib

# For GPU support
pip install cupy
```

## File Structure Commands
```bash
# List all notebooks
ls *.ipynb

# List model files
ls *.pkl

# Check common utilities
ls common/

# Check datasets
ls dataset/
```

## No Testing/Linting Infrastructure
- **No test framework** found (no unittest, pytest, etc.)
- **No linting tools** configured (no flake8, black, mypy, etc.)
- **No Makefile or build scripts** present
- **No CI/CD configuration** found

## Development Workflow
1. Open Jupyter notebook interface
2. Navigate to desired chapter notebook (ch01.ipynb - ch08.ipynb)
3. Execute cells interactively
4. Educational codebase - experiment with code and observe outputs
5. Each notebook contains all code from the corresponding chapter

## GPU Mode
To enable GPU acceleration:
1. Edit `common/config.py`
2. Change `GPU = False` to `GPU = True`
3. Ensure CuPy is installed
4. Restart notebook kernel to apply changes

## Working with Model Files
The .pkl files contain trained model parameters:
- `cbow_params.pkl` - CBOW model from ch04
- `Rnnlm.pkl` - RNN language model from ch06  
- `AttentionSeq2seq.pkl` - Attention seq2seq model from ch08

These can be loaded in the notebooks for inference or continued training.