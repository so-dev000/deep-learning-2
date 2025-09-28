# Code Style and Conventions

## File Encoding
- All Python files start with `# coding: utf-8`
- Japanese comments and documentation are common

## Import Conventions (Updated Structure)
- **Legacy approach removed**: No more `sys.path.append('..')` - this has been cleaned up
- **Standard imports**: Direct imports from `common.*` and `dataset.*` packages
- **Notebook structure**: Local classes defined within notebooks where needed
- **Comments for references**: Uses `# Note: ClassName is defined in the filename.py cell above` pattern

## Jupyter Notebook Conventions
- **One cell per original Python file**: Each chapter's code is organized with clear cell separation
- **Markdown headers**: Each code cell preceded by markdown cell with filename (e.g., `## train.py`)
- **Class definitions**: Key classes defined in early cells, referenced in later cells
- **Import organization**: Common imports at top of each cell, local references via comments

## Naming Conventions
- **Classes**: PascalCase (e.g., `TwoLayerNet`, `MatMul`, `Affine`)
- **Functions/Variables**: snake_case (e.g., `max_epoch`, `batch_size`, `learning_rate`)
- **Constants**: UPPER_CASE (e.g., `GPU`)

## Class Structure Pattern
Neural network layers follow consistent pattern:
- `__init__`: Initialize parameters (`params`) and gradients (`grads`)
- `forward`: Forward propagation method
- `backward`: Backward propagation method
- `params`: List of learnable parameters
- `grads`: List of corresponding gradients

## Comments
- Mix of Japanese and English comments
- Japanese used for educational explanations
- English for technical parameter names
- **Reference comments**: Added to indicate class dependencies between cells

## Code Organization
- **Notebook-based**: Educational content organized in interactive notebooks
- **Modular design**: Clear separation of concerns maintained
- **Educational clarity**: Prioritized over optimization
- **Sequential execution**: Designed for step-by-step learning in notebook environment
- **Self-contained**: Each notebook contains all necessary code for its chapter

## File Structure
- **Utility modules**: Remain as `.py` files in `common/` and `dataset/`
- **Chapter content**: Converted to `.ipynb` notebooks
- **Model persistence**: `.pkl` files for trained models