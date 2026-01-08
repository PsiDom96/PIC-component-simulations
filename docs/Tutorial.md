# Tutorial
### Includes
1. GDSFactory Toturial Notes
2. Tidy3D Tutrial Notes
3. 

## GDS Factory Tutorial
Find the GDSFactory tutorial on their [Getting Started](https://gdsfactory.github.io/gdsfactory/developer.html#tutorials) page.

**Read** `env_setup.md` in the docs folder to understand how to use GDSFactory tutorial notebooks on VSCode using local venv.


---

### 0. Python

#### Classes
Gdsfactory already has some pre-defined classes


All the other classes (Component, ComponentReference, Port ...) are already available in `gf.typings`

When using gdsfactory, you will write functions instead.


To use gdsfactory and PDK,

```python
import gdsfactory as gf

gf.gpdk.PDK.activate()
```

#### Functions

Add `type annotations` to your functions to clearly define what are the input/output types (string, int, float ...).

```python
def double(x: float) -> float:
    return 2 * x
```

#### Factories
A factory is a function that returns an object. In gdsfactory many functions return a `Component` object.

```python
def bend(radius: float = 5) -> gf.Component:
    return gf.components.bend_euler(radius=radius)
```

#### Ipython tricks:

The most common trick that you will see is that we use `?` to see the documentation of a function or `help(function)`.

```python 
gf.components.coupler? # or,

help(gf.components.coupler)
```
To see the source code, use
```python
gf.components.coupler??
```

To time the execution time of a cell, you can add a `%time` on top of the cell.

```python
%time     # this is a "decorator" (see Tutorial)
def fucntion() -> None:
    print('Runtime will display above this text')
```

### 2. Klayout

[KLayout](https://www.klayout.de/build.html) is a powerful open-source layout viewer and editor widely used in the semiconductor industry.

In the GDSFactory code-driven workflow, you define components, circuits, and reticles using Python or YAML. To enable rapid design iteration, GDSFactory includes a KLayout macro extension, which runs directly inside KLayout. This allows you to visualize your layouts instantly: when you call `component.show()` in Python, your GDS layout is automatically displayed in KLayout.

> To do: 
>* get Klayout working
>* go through geometry tutorial
>* simulate a MZI

