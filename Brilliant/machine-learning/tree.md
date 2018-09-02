## Tree

### Tree regression
- Regression trees are generated recursively, by continuously splitting the space containing the data we already have.
- The final endpoints in a tree, or spaces which contain no divisions, are known as leaves
- One limitation of the strategy explained is that it limits how spaces can be partitioned, 
  - For a set of partitionings to come from a tree, each section must be produced by splitting another space in half with a partitioning perpendicular to one axis. 
  This is because each division may only use one variable.
- A problem which becomes immediately apparent in regression trees is overfitting. 
By adding enough leaves to our tree we can easily reduce the SSE to zero, 
just by making sure that each leaf only contains one point from our training data, 
but this level of complexity has several repercussion

### Tree classification
- Similar to tree regression, classification is built on training data. 
- Each leaf assigns points to the most common class it contains. 
- Information gain, the rate of unmixing the data points at a node.
- Common error functions
  - Classification error function
  - Gini index
  - Cross entropy
- Gini index and cross entropy are better than classification error function, this might sound counterintuitive but while tree building the algorithm does not look forward instead it does what is best at the moment.

### Pros and cons
- Pros
  - Simple to understand
  - While trees do produce blocky results, they have the advantage of roughly fitting every function. Like a one size fits all suit, they might not be pretty, but they will work on nearly anything.
  - Another benefit of trees is their natural use of qualitative variables.
  - Applying increasing functions such as log/ exp/ square will not affect the decision tree's SSE  

- Cons
  - One limitation of trees is the natural blockiness of their predictions. It is rare for natural events to share in this blocky nature, so generally trees make relatively inaccurate predictions on data
  - It can be easily overfit to training data
  
### Bagging (Bootstrap aggregatiom)
- Tree based algorithms are inconsistent in nature, even a slight change in training data can lead to different trees for same set of data.
- Instead of having one tree we can have a multitude of similar trees, then taking the agregate of the result.
  - It helps in smoothening any ambiguity in the results
  - But it becomes hard to interpret because it gets rid of the decision chain.
  - In order have different trees we will need different data, so we will sample data from the full data set. If there are N poiints then we will take N samples.
  - Bagging becomes more effective when the trees are varied, because if the trees are similar then each tree will carry the same error and the result will be ineffective.
  - **Random forest** is an improvised version of the above algorithm, if there are p predictor variables then it will choose m variables to create a tree. Hence no variable will dominate the tree construction.
  
### Boosting
- In bagging, aggregates are computed to smoothen the oddity by trees but in boosting each tree is designed to make up for the fault in the previous tree. 
- Boosting works by continuously correcting for the errors of previous trees, so it is well equipped to handle a systemic error in tree estimates. As the trees build up, they will put increasing importance on making up for this error, until it vanishes.
- If it is likely for the data set to include very inaccurate numbers, it’s important to have a model which will strongly resist overfitting data. After all, if it molds itself to the data too closely, it will give a lot of weight to obviously wrong values.
- In the above case, Therefore, the better model for the situation is bagging. Although boosting will overfit slowly, it is definitely capable of perfectly fitting itself to data as the number of trees increases

### Resourcce
* [Decision tree](https://www.youtube.com/watch?v=LDRbO9a6XPU)
