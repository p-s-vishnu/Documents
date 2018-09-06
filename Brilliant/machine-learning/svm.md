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

### Non linear decision boundaries
- Loosing our training data won't cause much problem until we have the set of dot product of training data. These specify the degree of similarity between vectors.
- The above is a type of Kernel, it is easier to define a valid kernel function and then calculate boundary through it.
- The major benefit of a kernel function is that it allows us to have all of the benefits of increasing dimensionality without actually calculating dozens or hundreds of new dimensions.
- Some kernels, such as the radial basis kernel, can actually only be expressed as the dot product in an infinite number of dimensions.
- Examples 
  - Linear
  - Polynomial
  - Laplacial
  - Radial basis
  
### More than two classes
- SVM by itself is incapable of classifing more than two classes.But multiple simple classifiers can be used to split many
- For each pair of points there will be n*(n-1)/2 hyperplanes where n is number of classes.
- If the classifier is perfect then the max poll of all the hyperplanes will be always correct.
- An alternative for one vs one classifier is one vs many classifier.
- The confidence of a classifier is simply the magnitude of w.x - b.

### Connection to logistic regression
- While plotting a graph between hinge loss function and logistic classifier, we find that both the functions are nearly same. The are able to less affected by ouliers.
- Logistic regression is useful when there is no distinction between different classes. Whereas SVM can be employed in the counter case.

## Kernels

### Intro to kernels
- Two vectors can be compared for similarity using 
  - dot product
  - distance between them, exp( -||x-y||^2 ) 
- A kernel is an equation of vector with certain property. The above are example of Kernel.
- Feature space is the set of possibile values that an object of observation can have.
- Another example of kernel, it is any inner prodduct of two vectors in a feature space.
- k3(x,y) = k1(x,y) + k2(x,y) 
- Kernel Properties
  - Symmetric in nature
  - K(x,x) will be >= 0
  - They follow Cauchy-Schwartz inequality
- It’s important to note that the mappings that correspond to these functions can be exotic. The Radial Basis Function, for instance, actually corresponds to the dot product in an infinite number of dimensions
