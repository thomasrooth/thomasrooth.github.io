# Loss and Accuracy

Now that I have some experience using fastai to create models, I started exploring different methods of investigating the effectiveness of the models I was designing. I was incredibly surprised by the sheer number of pretrained models available for use in fastai!

![](/images/models.JPG "Different pretrained models available in fastai")

The resnet18 model is fast and effective enough for the classification models that I'm dealing with now. I could also implement the resnet34 but in his lecture Jeremy Howard suggests that we keep it simple for the time being. He always starts with the most basic models when approaching a classification problem.

## Loss

A loss function compares the predicted and actual output values of a classification model to determine how the model needs to change. This is implemented in fastai in the fine_tune() method which iteratively improves the pretrained model using the loss function.
