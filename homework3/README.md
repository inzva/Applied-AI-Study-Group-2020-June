
## Homework 3 - Text Generation

- This homework will make you familiar with existing scraping tools and using them to scrape an NLP dataset from web. 

- It will optionally make you familiar with state of the art Natural Language Generation architecture and some niche Natural Language Processing tools such as the attention mechanism. This is a quite valuable kind of knowledge today.

- We will take a text dataset (a.k.a. corpus. corpus means a list of documents, like a list of articles) and we will train a network that is able to generate such text that, the generated text is indistinguishably similar to the example documents (articles) in the dataset. We will need to format our dataset file in proper style, since we will use a prepared module as the first step.

- Note that this homework is not a liability, instead it is only to benefit your skills. 



#### The main steps: Scraping Data and training a model:

1- Use a specialized scraping tool for your task. One example is this newspaper scraping tool, it is a good and easy one to work with, you can try it on some news sites: https://github.com/codelucas/newspaper

2- Once you scrape the text data, you need to prepare your data just as we did in class. Declare a list, fill it with document (article) instances and consider each of the documents as one training example. 

3- There are different approaches for this problem. We will use the Character based RNN to be on the same page as the study group. It will be simple. If you want, you can use a Transformer module later, or even write your own Transformer network.

4- Check the repository: https://github.com/minimaxir/textgenrnn. This repository includes a very easy to use module, on which, you can train a previously-constructed neural network with your own data. Clone the repo to your computer, follow the instructions to train the network from your dataset file. (your dataset file is a text file that you should create.)

5- Your dataset file should be formatted right. In detailed words, you should open a .txt file, where you **write each data instance on a line**. So do NOT have any newline (enter, \n) character inside any of your training examples. If your examples include the character '\n', remove them with the appopriate preprocessing algorithm. Each of your training examples should be seperated by a newline ('\n') character.

6- If you are confused about the proper format, check the example dataset file in the repo: https://github.com/minimaxir/textgenrnn/blob/master/datasets/hacker_news_2000.txt

7- After your dataset.txt file is formatted right, you should be able to use train_from_file method to train the network on your dataset. Train your model with that method.

8- Print the results and enjoy.



#### Optionally: Trying to understand the Architecture of the Transformer and Changing Hyperparameters :

9- Now that we used a prepared Character Based RNN module, we can get more technical, using the Transformer. It is also time to be able to set some hyperparameters of the network. 

10- Try to understand a bit of the transformer. This is just to be able to modify the hyperparameters. To try to understand the Transformer you can check these:
https://medium.com/inside-machine-learning/what-is-a-transformer-d07dd1fbec04 (high level overview)
http://jalammar.github.io/illustrated-transformer/ (more technical depth)
There is also extra material at the end of this readme file.


11- Clone the repository https://github.com/kimiyoung/transformer-xl to your working environment. This repo includes a Transformer architecture and running shell scripts, which you can use to modify the architecture's hyperparameters.

12- Check the file pytorch/run_enwik8_base.sh . This file can only be ran on linux or macos operating systems. If you use Windows, you can install git-bash and run the .sh from there, hoping it to work. Or use google colab, which is a linux based environment. You can do everthing that is mentioned here on colab.

13- Modify the file run_enwik8_base.sh . The problem is that the file does not take **your** dataset as input, so change the data parameter on the file. Also, make the network parameters smaller. Current parameters are only eligible to be ran on 4 GPUs.

14- Be sure your data is formatted right. To be sure, run getdata.sh and examine the downloaded example dataset files.

15- Run the file run_enwik8_base.sh. It should train your model.

16- To print generated text from the model, check the issue https://github.com/kimiyoung/transformer-xl/issues/49 on the repo. You can find some code there, which you can include to print the generated text.


#### Optionally 2: Coding your own training scheme, using the Transformer classes provided in pytorch.

You have worked with the hyperparemeters of the Transformer model. You can also use pytorch's transformer classes to develop your own training schemes:
https://pytorch.org/tutorials/beginner/transformer_tutorial.html


#### Optionally 3: Implement your own Transformer from scratch. Hardcore but doable!

It is also possible to implement a Transformer from scratch. It is a highly valuable study to implement such network since it is quite new and technically advanced. To implement the Transformer, you can check:
https://towardsdatascience.com/how-to-code-the-transformer-in-pytorch-24db27c8f9ec



#### Materials on Text Generation and other stuff:

	a- Text Generation without a transformer (entry level): https://medium.com/@shivambansal36/language-modelling-text-generation-using-lstms-deep-learning-for-nlp-ed36b224b275

	b- Text Generation without a transformer (more intermediate): https://medium.com/phrasee/neural-text-generation-generating-text-using-conditional-language-models-a37b69c7cd4b

	c- To understand encoder-decoders: https://medium.com/@keremturgutlu/semantic-segmentation-u-net-part-1-d8d6f6005066

	d- To understand transformers (high-level overview): https://medium.com/inside-machine-learning/what-is-a-transformer-d07dd1fbec04

	e- To understand transformers (more low-level, technical): http://jalammar.github.io/illustrated-transformer/

	f- Transformer XL (an upgraded version of the transformer): https://towardsdatascience.com/transformer-xl-explained-combining-transformers-and-rnns-into-a-state-of-the-art-language-model-c0cfe9e5a924
