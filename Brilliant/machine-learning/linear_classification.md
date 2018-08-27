## Linear classification
+ The goal of any classification algorithm is to find the class a data point is most likely to belong to.

**Indicator Matrix**
1. The classification in indicator matrix is done by calculating the maximum probability of a data point for each class.
2. [Qualitative data](https://www.youtube.com/watch?v=fKEkb_wO1OA) 
3. [One hot encoding](https://www.youtube.com/watch?v=v_4KWmkwmsU), is a method in which categories are encoded into vectors of 0 and 1. 
The name one hot implies, only the corresponsing class will have a '1' and rest all will be zero. A set of these vectors is represented using a matrix.

**Logistic Classification**
1. The probability that all of the known points have the class they do, is what is maximized by the logistic classification algorithm. The process is known as the *maximal likelihood method* because we are finding the highest possible likelihood for a sigmoidal probability function.
2. Generally, classifications are made by setting a threshold probability which divides two classes.
3. Just as it is useful to turn a linear function into a sigmoidal one for the purpose of calculating probabilities, it is often useful to do so reverse in order to facilitate mathematics.
4. [Logit](https://en.wikipedia.org/wiki/Logit), it is the inverse of sigmoid function.
