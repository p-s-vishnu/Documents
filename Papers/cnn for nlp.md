## Convolution neural network for Natural language procesing

### Intro 
* CNN are very effective in classification problems. The AI systems like Humanoid robots are based on embedded systems which are limited in memory, processing power,etc. 
* In this paper, results are presented of compressing the efficient convolutional neural networks for sentiment analysis.
* Here the method is responsible for deploying compressed network to [Xilinix - FPGA](https://www.xilinx.com/products/silicon-devices/fpga/what-is-an-fpga.html).
* It helps to reduce memory of NLP model footprints on embedded devices. 

### Convolutional Neural Network

  * [Quantization process](http://proceedings.mlr.press/v48/linb16.pdf)

  * [Pruning](https://jacobgil.github.io/deeplearning/pruning-deep-learning), it is the process fine-tuning the network for smaller network size.

### Dataset
  * Data set used for experimentation :
   1. MR : [Movie Review data for sentimental-analysis](http://www.cs.cornell.edu/people/pabo/movie-review-data/)
   2. SST1 : Stanford Sentiment Tree bank, same as MR but with train/dev/test splits. It is having 5 labels (Very positive, positive, neutral, negative, very negative). [Link](http://nlp.stanford.edu/sentiment/)
   3. SST2 : Same as above but neutral labels are removed.
   4. Subj : Subjectivity dataset where the task is to identify whether the sentence is Subjective(Opinion) or Objective(Facts). [Link](http://cogcomp.cs.illinois.edu/Data/QA/QC/)
   5. TREC : TREC question dataset where the objective is to classify a question into six different question catgories.
   6. CR : Customer review dataset. [Link](http://www.cs.pitt.edu/mpqa/)
   
   CV : 10-fold cross validation is performed
   data(where CV is not done) : 10% of training data
 
### Network Architecture

  * FPGA Implementation
  
### Precision Reduction
  * The precision reduction is applied at weights of layers and outputs of activation functions. 
  * Model used for reduction : 
    * [Embedding](https://developers.google.com/machine-learning/crash-course/embeddings/video-lecture)
    * 2 dense layers : It is a fully connected layer, so all that the neurons in a layer are connected to those in a next layer.
    * 2 CNN
  
### Experiments
 * FGPA results 

### Conclusions and future work
* The results of the experiments show that the size of the model may be reduced more than 84% with the little performance degradation of approximately 1%.
* Word embeddings can be compressed even more reaching 93%.

### References
* [Neural network](https://www.youtube.com/watch?v=aircAruvnKk)
* [CNN](https://brilliant.org/wiki/convolutional-neural-network/)
* [How pruning can help](https://www.youtube.com/watch?v=3yOZxmlBG3Y)
* Cross validation error : [Explanation 1](https://www.youtube.com/watch?v=sFO2ff-gTh0), [Explanation 2](https://www.youtube.com/watch?v=hihuMBCuSlU)
* [IEEE - Sentimental analysis using CNN](https://ieeexplore.ieee.org/document/7363395)
* [Neural net for NLP 2017](https://www.youtube.com/watch?v=vnzKAhs7nds&t=210s)
* Feature maps : [Quora](https://www.quora.com/What-is-meant-by-feature-maps-in-convolutional-neural-networks)
* [Precision and recall](https://developers.google.com/machine-learning/crash-course/classification/precision-and-recall)
* How CNN can be used for Text classification [Quora](https://www.quora.com/How-are-convolutional-neural-networks-used-in-natural-language-processing)
* [Basics : Hill climbing algorithm](https://www.youtube.com/watch?v=oSdPmxRCWws)
* [CMU Neural network for NLP](https://www.youtube.com/watch?v=vnzKAhs7nds)
* [Visualization : Building a feature map from feature filter/window](https://www.youtube.com/watch?v=KiftWz544_8)
