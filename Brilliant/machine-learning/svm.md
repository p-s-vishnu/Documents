## Support vector machine

### Hard margin support vector 
- For every *n* dimensional plane there can a infinite number of *n -1* dimension hyperplanes to divide it into half.
- An interesting property, weight vector w of hyperplane is always perpendicular to the it. 
- From the infinite number of hyperplane how to choose the right one ? 
  - Maximum margin classifier, select the hyperplane which divides two classes also it should have greatest margin 
  from points of each class.
- Maximum marginal classifier can also be termed as perceptron of optimal stability. It is similar to perceptrons but it has an 
additional property to maximize the margin.
- The points away from the margin hyperplane does not have much role, which leads to
  - Only small percentage of points are responsible for margin and in some way it is beneficial 
  - Therefore it is more likely to face high variance
  - The minority of points that affect the hyperplane are known as *support vectors*
- As one would expect, the actual mathematics of maximal margin classification involve solving a maximization problem. 
Maximizing 2 /||w|| or minimizing ||w||.
- It can become computationally costly with more number of data points.
- But performs even well with large number of predictor variables, outliers and noise.
