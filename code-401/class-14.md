# Data Visualization: matplotlib-tutorial 


### useful methods & arguments:

- `plt.figure(figsize=(10,6), dpi=80)`

- `plt.plot(X, C, color="blue", linewidth=2.5, linestyle="-")`

- when limits of the figure are a bit too tight and we want to make some space in order to clearly see all data points.
```python 
plt.xlim(X.min()*1.1, X.max()*1.1)
plt.ylim(C.min()*1.1, C.max()*1.1)
```

- to change ticks such that they show only these values. , we can also provide a corresponding label in the second argument list. 
```python
plt.xticks([-np.pi, -np.pi/2, 0, np.pi/2, np.pi],
       [r'$-\pi$', r'$-\pi/2$', r'$0$', r'$+\pi/2$', r'$+\pi$'])

plt.yticks([-1, 0, +1],
       [r'$-1$', r'$0$', r'$+1$'])
```
- adding legends
```python
# you must add labels at first to the x and y plots as arguments
plt.legend(loc='upper left', frameon=False)
```
- you can annotate some points
```python
#check out
plt.annotate()
```

### Subplots

With subplot you can arrange plots in a regular grid. 
```python
import matplotlib.pyplot as plt

plt.subplot(2,2,1)
plt.subplot(2,2,3)
plt.subplot(2,2,4)

plt.show()
```

### Axes

Axes are very similar to subplots but allow placement of plots at any location in the figure. So if we want to put a smaller plot inside a bigger one we do so with axes.

### types of plots:
1. regular plot
2. scatter plot
3. bar plot
4. contour
5. imshow
6. quiver plot: 2D field of arrows
7. pie chart
8. grid
9. multiplot: several plots at once
10. polar axis
11. 3d plots
12. text