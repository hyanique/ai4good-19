## Multi-Layer Percptron

## Summary

- Just a basic feed-forward neural network, _fully_ connected.
- It can do the supervised learning as well as the unsupervised one.
- Motivation: neurons & function approximation
- Some Limitations
  - Too may parameters...
  - Prone to overfit (so lets bring in regularization!)
  - Cannot do parallel computation
- Training: use the backpropagation approach, which is merely multivariate chain rule of (partial) derivtives.

### Algorithm

Nothing Fancy, check study note

### Implementation

#### Hints

- For dot product $x \cdot y$: `x.dot(y)`
- For matrix transpose $ x^\top$ use `x.transpose`
- Keep track of the dimensions of all numpy arrays
- Start with a simpleMLP, then to a standard one.
- It can be hard, brag some coffee.

#### Coding

A not-running undebugged version can be find in simpleMLP.py. The file is for practice algorithm implementation only and, unlike k-mean and k-NN, is not supposed to be a functional code.

### Using the Libraries

#### Sci-Kit Learn

Just like linear transformation (not linear functional!) and manifold, the MLP can be view as a mathematical model that can be used in the field of ML. So there is no supersing that `sklearn` got their MLP prepared for both classification and regression.

Link [here](https://scikit-learn.org/stable/modules/classes.html#module-sklearn.neural_network) :no_mouth:

**MLP regression**

Create a swiss roll and do the regression!

No... swiss rolll is for _manifold learning_. Use "Friedman" or "boston housing" or "load_linnerud". (Or come up with some fancy function then feed it to `make_regression`)

**MLP classification**

1. learning rate
2. regularization penalty coefficient
3. visualization of some weight......

#### PyTorch

This PyTorch, what would you expect?

...Well, you just instantiate the model and play with datasets and hyperparmeters

### Reflections

God knows how long it takes me to figure out how mathplotli works......

Must be some way to tune the hyperparmeters instead mannually do those stuffs

### Note to Self

1. sklearn: `make_moon` and `make_circle`
   > make_circles and make_moons generate 2d binary classification datasets that are challenging to certain algorithms (e.g. centroid-based clustering or linear classification), including optional Gaussian noise. They are useful for visualisation. make_circles produces Gaussian data with a spherical decision boundary for binary classification, while make_moons produces two interleaving half circles.
2. MinMaxScaler vs. StandardScaler: [link1](https://www.quora.com/Minmaxscaler-vs-Standardscaler-Are-there-any-specific-rules-to-use-one-over-the-other-for-a-particular-application), [link2](http://rajeshmahajan.com/standard-scaler-v-min-max-scaler-machine-learning/)

3.matplotlib tricks

- To hide axis value, do this: `ax.set_yticklabels([])`
- To add some fancy text in the subplot, do this: `axis.text(pos_x, pos_y,text, size=12, horizontalalignment='right')`
- To set some fashionable (blah) labels, use this: `ax.set_ylabel(name,size=15,labelpad=12)`

4. Ploting 3D

- `from mpl_toolkits.mplot3d import Axes3D`
- Use `plot_trisurf` if you have xx, yy, zz as 1-dim arrays. Use `plot_surface` if you have `xx,yy=meshgrid(...)` and has resultingz as 2-dim arrays.
- Read us: [link 1](https://matplotlib.org/gallery/mplot3d/surface3d.html), [link 2](https://matplotlib.org/gallery/mplot3d/scatter3d.html), [link 3](https://jakevdp.github.io/PythonDataScienceHandbook/04.12-three-dimensional-plotting.html)
- The color maps [doc](https://matplotlib.org/tutorials/colors/colormaps.html)
