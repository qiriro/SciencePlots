Science Plots
=============

*Format Matplotlib for scientific plotting* 

This repo has Matplotlib styles to format your plots for scientific papers, presentations and theses.

Installation
------------

Put the ``*.mplstyle`` files in your Matplotlib style directory. If you're not sure where this is, in an interactive python console type:

```python
import matplotlib
print(matplotlib.get_configdir())
```

You should get back something like ``/home/garrett/.matplotlib``. You would then put the ``*.mplstyle`` files in ``/home/garrett/.matplotlib/stylelib/`` (you may need to create the ``stylelib`` directory). If you're on macOS, you can run:

```bash
mkdir -p ~/.matplotlib/stylelib/
cp *.mplstyle ~/.matplotlib/stylelib/
```

Using the Styles
----------------

``science.mplstyle`` is the main style from this repo. Whenever you want to use it, simply add the following to the top of your python script:

```python
import matplotlib.pyplot as plt
 
plt.style.use('science')
```

You can also combine multiple styles together by:

```python
plt.style.use(['science','ieee'])
```

In this case, the ``ieee`` style will override some of the parameters from the main ``science`` style in order to configure the plot for IEEE papers (column width, fontsize, etc.). 

To use any of the styles temporarily, you can use:

```python
with plt.style.context(['science', 'subfigure']):
    plt.plot(x, y)
plt.show()
```

Contribution
------------

Please feel free to add to this repo! For example, it would be good to add styles for different journals or perhaps new color cycles.

Examples
--------

![alt text](examples/figures/fig3.jpg)

![alt text](examples/figures/fig1.jpg)

![alt text](examples/subfigure-example.png)

**Note:** See the ``examples/`` directory for more!
