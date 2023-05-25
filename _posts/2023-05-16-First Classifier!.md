# My First Classifier!

I just finished writing my first classifier in a Jupyter Notebook using fastai based on the example provided in the 'Is it a bird?' lesson. It was surprisingly simple! My task was to adapt the classifer so that it could identify 10 differnet animals. 

I chose the following animals:

{% include info.html text="I selected these animals as they are distinct from each other to make classification easier." %}

1. cat
2. eagle
3. turtle
4. cow
5. horse
6. anteater
7. shark
8. penguin
9. crocodile
10. dragonfly


## Modified image searcher for classification.


    searches = 'cat', 'eagle', 'turtle', 'cow', 'horse', 'anteater', 'shark', 'penguin', 'crocodile', 'dragonfly'
    path = Path('Animal Classifier')
    from time import sleep

    for o in searches:
        dest = (path/o)
        dest.mkdir(exist_ok=True, parents=True)
        download_images(dest, urls=search_images(f'{o} photo'))
        sleep(6)
        resize_images(path/o, max_size=400, dest=path/o)
    

Now the `DataBlock` containts the data of the 10 different images. The below image shows a batch from the datablock.

![](/images/batch.JPG "Batch from DataBlock")


I am still in awe that it only takes a few minutes to train a working classifier of 10 different animals. Fine tuning the model takes less than 5 minutes as shown by the table below.

| epoch  | Train Loss | Valid Loss  | Error Rate |  Time |
| ------ | ---------- | ----------- | ---------- | ----- |
|   0    |  0.537959  |  0.418375   |  0.122727  | 01:32 |
|   1    |  0.329051  |  0.387139   |  0.100000  | 01:34 |
|   2    |  0.205212  |  0.393351   |  0.100000  | 01:34 |


Now I just need to analyse my results using t-SNE and confusion matrices.
