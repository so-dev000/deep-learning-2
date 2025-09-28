# Task Completion Guidelines

## When Task is Completed

Since this is an **educational codebase without formal development infrastructure**, there are minimal completion requirements:

### No Formal Testing
- No test suite to run
- No automated testing framework present
- Verification through manual notebook execution

### No Linting/Formatting
- No linting tools configured
- No code formatting requirements
- Follow existing style patterns manually

### No Build Process
- No build system present
- No compilation or packaging steps required

### Verification Steps for Jupyter Notebooks
1. **Notebook Execution**: Run notebook cells to ensure they execute without errors
2. **Visual Verification**: Check that plots and outputs appear as expected
3. **Import Verification**: Ensure all imports resolve correctly
4. **Code Review**: Ensure changes follow existing conventions
5. **Educational Purpose**: Verify changes maintain educational clarity

### Typical Workflow After Changes
```bash
# Start Jupyter notebook server
jupyter notebook

# Open specific chapter notebook
# ch01.ipynb, ch02.ipynb, etc.

# Execute cells sequentially
# Verify outputs and plots appear correctly
# Check for any runtime errors

# Alternative: Command line execution
jupyter nbconvert --execute --to notebook ch01.ipynb
```

### Common Verification Tasks
- **Import Resolution**: Ensure `from common.*` and `dataset.*` imports work
- **Class Dependencies**: Verify classes defined in earlier cells are accessible
- **Model Loading**: Check that .pkl files can be loaded when referenced
- **GPU Mode**: Test both CPU and GPU modes if applicable

### Git Operations
- Standard git commands for version control
- No pre-commit hooks or automated checks
- Manual review of changes before commits

### Special Considerations
- **Maintain educational clarity** over optimization
- **Preserve Japanese comments** and documentation style
- **Ensure GPU/CPU compatibility** through common/np.py abstraction
- **Keep implementations simple** and understandable for learning purposes
- **Sequential execution**: Notebooks designed to run cells in order
- **Self-contained chapters**: Each notebook should be independently runnable

### File Structure Considerations
- **Utility modules** (`common/`, `dataset/`) remain as Python files
- **Chapter content** organized in Jupyter notebooks
- **Model files** (.pkl) accessible from root directory
- **No chapter directories** - everything consolidated at root level