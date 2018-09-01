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
