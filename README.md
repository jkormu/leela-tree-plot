# leela-tree-plot
Ugly tools for creating beautiful LC0 search tree plots

## What?
leela-tree-plot is a set of python functions to visualize search trees of chess engine LC0 (Leela chess zero).
The plots are created with Plotly. Plots are written in html format and are interactive.

leela-tree-plot depends on modified LC0 binary that is capable of saving the search graph as a gml-file.
These tools:
- call lc0 exes to run searches
- read gml-files
- run Buchheim's tree layout algorithm
- plot the search tree as Plotly html plot

![Alt text](images/example_plot.png?raw=true)

## How?
It is assumed you are familiar with LC0 and know how to build it:
- get dependencies (tested with python 3.7):
```
python-chess              0.28.3
plotly                    4.1.1
numpy                     1.17.2
networkx                  2.3
jupyter notebook (optional for running example.ipynb notebook)
```
- Clone and build modified LC0 version capable of writing search tree as a gml-file:

```
git clone -b 0.22_gmltree --recurse-submodules https://github.com/jkormu/lc0.git lc0_gmltree 
cd lc0_gmltree
sh build.sh
``` 
- clone leela-tree-plot
- go through the examples in example.ipynb and start creating your own plots

