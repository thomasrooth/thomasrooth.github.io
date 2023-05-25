## Natural Language Processing
This is a collection of concepts and resources that I found fascinating during Jeremy Howard's fastai lesson on NLP.

What does NLP do? The first language model developed, ULMfit, was attempting to guess the next word in a Wikipedia article. NLP models need to understand how language works, how things are expressed and what is true.


{% include info.html text="The model was able to predict the next word of any word in any article 36% of the time. Impressive!" %}


The first task Jeremy Howard did for a fastai course was adapting ULMfit to detect sentiment in text. He fine tuned the ULMfit model using IMDb movie reviews. The model was then able to predict the next word in IMDb movie reviews.


{% include alert.html text="Around this time, a new architecture was developed - Transformers!" %}


NLP can be used for classifying documents. A document is any text that is inputted into an NLP document.

This is used for:
- Sentiment analysis
- Author identification
- Legal discovery
- Organising documents by topic
- Triaging inbound emails



### Hugging Face Model Hub
The [Hugging Face](https://huggingface.co/) model hub contains a variety of pretrained models that are NLP specific. You can find a pretrained model for the specific document that you are dealing with.



![](/images/hf-logo-with-title.png " ")



### Tokenisation and Numericalisation
Tokenisation breaks the document into words (but not really words). Words can be broken into smaller chunks if they are overly complicated or uncommon. Numericalisation is then used to convert those tokens into numbers. This is done using a simple dictionary lookup.




### Overfitting and Underfitting

![](/images/fitting.jpg "Examples of fitting, overfitting and underfitting.")

Overfitting a model means that the model is fit specifically to the training data. The model is so precise to the training data that it doesn't represent the data in general. Underfitting means that the model doesn't reflect the data at all. Typically this means that the order of the model is too low. The trend of the model doesn't represent the trend in the data. This emphasises the important of separate training and validation sets for model testing. A model may appear incredibly accurate when tested with the same data used to train it, but it is actually overfit to the training data.








