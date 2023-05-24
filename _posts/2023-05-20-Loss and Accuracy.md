# Assessing Model Suitability

> "Machine intelligence is the last invention that humanity will ever need to make" - Nick Bostrom

Now that I have some experience using fastai to create models, I started exploring different methods of investigating the effectiveness of the models I was designing. I was incredibly surprised by the sheer number of pretrained models available for use in fastai!

![](/images/models.JPG "Different pretrained models available in fastai")

The resnet18 model is fast and effective enough for the classification models that I'm dealing with now. I could also implement the resnet34 but in his lecture Jeremy Howard suggests that we keep it simple for the time being. He always starts with the most basic models when approaching a classification problem.

## Loss

A loss function compares the predicted and actual output values of a classification model to determine how the model needs to change. This is implemented in fastai in the `fine_tune()` method which iteratively improves the pretrained model using the loss function.

For an image classification problem, fastai automatically uses a [Cross Entropy Loss Function](https://docs.fast.ai/losses.html). Model weights are iteratively adjusted to minimise this loss function. A perfect model will have a cross entropy loss of 0. The loss in the model can be tracked as the weights are iteratively updated by observing the output table of the `fine_tune()` method.

![](/images/finetune.JPG "Output of the finetune() method in fastai")

We can observe that the loss in the model when tested with both validation and training datasets reduces iteratively. We can also observe the accuracy matric which evaluates the accuracy of the model by comparing predicted to actual outputs. We can see that the model accuracy improved to 98% but cannot pass this threshold.

A confusion matrix is a great tool for visualising model accuracy. 

![](/images/confusion.JPG "Confusion matrix in fastai")

From this visualisation, we can see how accurate the classification model is. It is able to classify every animal image correctly except for one. The model predicted that one image was a penguin, when in fact it was a horse. While the cause of this error is unknown, it is an interesting observation to consider.

{% include info.html text="Did you know that horses and penguins look the same? I didn't..." %}
