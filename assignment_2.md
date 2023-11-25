I run the notebook on Google Colab because I had problems with working on the server and because I always got Cuda out of memory errors when training the models.

# Part 3

My fine tuned models could not load for some reason and I got errors that I had to train them to use them for predictions and inference even though I had already done it.
I am not sure if I did something wrong when saving the models, because the same saving method worked for part 1 of the first demo tutorial. This could also be due to the fact that I am not saving checkpoints of the model, but I decided not to do that in order to avoid out of memory errors on Google Colab.

# Part 4

In order to check which model performs better I parsed the text using the ud pipe tool to acquire its structure and compare the words recognized by the tool and the predicted tags that were given by the models. Both models did not recognize correctly most of the tokens of the sentence, and they both tagged most tokens as beginning_of_word, probably beccause this tag was more frequent in the training data. 

Even if my models could not be loaded the expected way, I would expect that distil BERT would probably not perform as well as Chinese BERT. Since this model is not specifically trained for Chinese language but is more focused on English, achieving high results in Chinese word segmentation would probably require fine tuning distil BERT on a chinese corpus/dataset.

Since Chinese Bert seems to be specifically pre-trained on Chinese text, it is more optimized for tasks targeting the Chinese language, like token classification/word dsegmentation. So, it would be expected to have high accuracy scores (at least higher than distil BERT) when performing on such a task.