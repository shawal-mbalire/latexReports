# LaTeX Reports Repository

This repository contains various LaTeX reports for electrical engineering experiments and labs.

## How to Compile LaTeX Files in Nonstop Mode

To compile a LaTeX document without stopping on errors (nonstop mode), use the following command in the terminal:

```bash
pdflatex -interaction=nonstopmode main.tex
```

This will generate a PDF file (`main.pdf`) in the same directory, even if there are minor errors.

### For Specific Reports

Navigate to the desired report folder and run the command. For example:

- For Circuit Analysis (10circuitAnalysis):
  ```bash
  cd 10circuitAnalysis
  pdflatex -interaction=nonstopmode main.tex
  ```

- For Analogue Labs (05analogueLabs):
  ```bash
  cd 05analogueLabs
  pdflatex -interaction=nonstopmode main.tex
  ```

### Using latexmk for Automatic Compilation

For more advanced compilation with automatic rerun for references and bibliography:

```bash
latexmk -pdf main.tex
```

This tool will handle multiple passes if needed for cross-references, TOC, etc.

### Prerequisites

- Install TeX Live or MacTeX (for macOS).
- Ensure all required packages are installed (e.g., circuitikz, pgfplots, siunitx).

### Git Hook

A pre-commit hook is set up to automatically compile the LaTeX documents before committing changes. If compilation fails, the commit will be aborted.

To enable the hook, ensure `.git/hooks/pre-commit` is executable (it should be after setup).