# machine_learning_project

This is a jupyter notebook where every cell needs to be run in order. Before running the notebook please unzip the archive folder.

I first create a list of dicitonaries with all the poems in order to create a table with all the poems, their topic or their form. I also preprocess the data and remove any unwanted information.

After creating one table for topics and one for forms, I create a merged table for everything, but in the end I proceed with only the topics dataset which I split in training and testing.

After that, I encode the labels and add special tokens to my tokenizer dictionary in order to recognize the <BOS>' and '<EOS>' tokens I add to the beginning and end of the poems respectively.

I prepare a custom Dataset class and load it with pytorch Dataloader.

After making sure everything works, I intialize my model with the necessary configurations, initialize the optimizer and scheduler, and define the training steps.

In order to compare with the results of the fine-tuned model I generate a text of length 30 with the raw model and then train it on my dataset. 

Lastly, I generate output in the same way I did with the raw model, but his time using the retrained model.
