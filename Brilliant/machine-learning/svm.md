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

### Soft margin vector machines
- Hard margin classifier breaks when supplied with inseparable data. Its solution is hinge loss function, it penalizes points that are on the wrong side of the classifier and return 0 for others.
- As *error* goes down the following will happen
  - ||w|| and hinge loss will decrease
  - margin will increase
  - incorrect classification will improve
- The error function is a useful tool in soft margin classification, but there are a few alternatives. One such alternative is to create a ‘slack’ variable, which quantifies the total amount by which wrongly classified points can err before the classifier is thrown out.
  - A large budget will allow the hyperplane to prioritize margin width over all else. 
  - A small one will force it to prioritize correct classifications.
- As the slack variable becomes large how will the number of support vectors generally change ? (It will increase)

