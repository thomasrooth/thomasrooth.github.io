# My First Classifier!

I just finished writing my first classifier in a Jupyter Notebook using fastai based on the example provided in the 'Is it a bird?' lesson. It was surprisingly simple! My task was to adapt the classifer so that it could identify 10 differnet animals. 

I chose the following animals:
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

{% include info.html text="I selected these animals as they are distinct from each other to make classification easier." %}\


## Modified image searcher for classification.

`searches = 'cat', 'eagle', 'turtle', 'cow', 'horse', 'anteater', 'shark', 'penguin', 'crocodile', 'dragonfly'
path = Path('Animal Classifier')
from time import sleep

for o in searches:
    dest = (path/o)
    dest.mkdir(exist_ok=True, parents=True)
    download_images(dest, urls=search_images(f'{o} photo'))
    sleep(6)
    resize_images(path/o, max_size=400, dest=path/o)`
    

