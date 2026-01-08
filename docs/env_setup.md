# Environment Setup

This document describes how the Python environment for this project is set up and how it is integrated with VS Code and Jupyter notebooks. The goal is to ensure a **reproducible, tool-aligned workflow** for photonic layout and simulation using GDSFactory (and later, simulation backends such as Tidy3D).

---

## Python Environment

- **Python version:** 3.10  
- **Virtual environment:** `.venv` (per-repository)
- **Platform:** Windows
- **Editor:** VS Code with Jupyter support

A dedicated virtual environment is used to isolate project dependencies and avoid conflicts with system-wide Python installations.

---

## Creating and Activating the Virtual Environment

From the root of the repository:

```bash
python -m venv .venv
.\.venv\Scripts\activate
```

After activation, the terminal prompt should indicate that .venv is active.

---

### Installing Dependencies

Dependencies are installed using pip. Once a stable environment is established, versions are pinned in requirements.txt.

```bash
pip install -r requirements.txt
```
>Note: At early stages of development, dependencies may be installed incrementally and frozen later using pip freeze > requirements.txt.

---

### Jupyter Kernel Registration (VS Code)

VS Code notebooks use Jupyter kernels, which must be explicitly registered for Python virtual environments.

After activating `.venv`, install `ipykernel` into the environment:

```bash
pip install ipykernel
```

Then register the kernel:
```bash
python -m ipykernel install --user --name gdsfactory-venv
```

This command:

1. Creates a Jupyter kernel tied to the Python interpreter inside .venv

2. Registers it for the current user

3. Makes it selectable in VS Code notebook kernel menus under the name `gdsfactory-venv`

---

### Selecting the Kernel in VS Code

1. Open a .ipynb notebook in VS Code

2. Click Select Kernel (top-right)

3. Choose: `gdsfactory-venv`

To verify the correct interpreter is in use, run the following in a notebook cell:

```python
import sys
sys.executable
```

The output should point to: 
```
...\<repo>\.venv\Scripts\python.exe
```

---

### Rationale

This setup ensures:

* Isolation of project dependencies

* Compatibility with GDSFactory’s recommended workflows

* Reliable execution of Jupyter notebooks in VS Code

* A clean foundation for later integration with electromagnetic simulation tools (e.g., Tidy3D)

--- 

## Next Steps

1. Work through the GDSFactory tutorial notebooks using the registered kernel

2. Validate component creation, visualization, and export workflows

3. Integrate simulation backends after layout workflows are well understood