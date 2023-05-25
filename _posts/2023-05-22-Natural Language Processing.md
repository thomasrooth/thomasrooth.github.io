## Natural Language Processing

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




Tokenisation breaks the document into words (but not really words).
- uncommon words split into small chunks

Numericalisation converts tokens into numbers.


### Overfitting and Underfitting
Use sklearn for regression
