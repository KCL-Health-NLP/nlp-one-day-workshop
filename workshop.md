# Natural Language Processing (NLP) - a one day introductory workshop<a name="top"/>
# Workshop material

*A one day workshop on NLP with a health record focus prepared for [MQ Mental Health Research](https://www.mqmentalhealth.org/) and [DATAMIND](https://datamind.org.uk/) by [King's College London Institute of Psychiatry, Psychology and Neuroscience](https://www.kcl.ac.uk/ioppn)*


## Contents

1. [Introduction](#introduction)
1. [Representing language: documents](#representing-language-documents)
1. [Representing words: vector semantics](#representing-words-vector-semantics)
1. [Playing with word embeddings](#playing-with-word-embeddings)
1. [Supervised machine learning for simple text classification](#XXX)
1. [Neural networks](#neural-networks)
1. [Generative AI](#generative-ai)

## Introduction
[[back to top]](#top)

- This repository contains all the material you will need for the NLP day on the Biostatistics and Health Informatics Youth Awards Programmeone day workshop
- The day will consist of six practicals to explore topics in NLP and neural networks
- Each practical will be introduced by short presentations of around 5 minutes each

**Python**

- Practicals will be in the Python programming language
- Don't worry if you don't know any Python, you do not need to write any code
- We will explain how to run the code, and talk you through each step
- We will run our Python code using Google Colaboratory (Colab), a cloud-based virtual compute service
- You will need a Gmail / Google account to use Colab
- If you do not have a Gmail account, [please create one now](https://support.google.com/mail/answer/56256?hl=en-GB) 

**Presentation**

- [Introductory presentation](./presentations/introduction.pdf) 

## Representing language: documents
[[back to top]](#top)

**Shakespeare's plays as vectors**
*Original idea from Jurafsky and Martin, [Speech and Language Processing](https://web.stanford.edu/~jurafsky/slp3/), Draft 3rd Edition.*

If we want to manipulate and analyse language computationally, we first need to find a way to represent language. We will start by looking at how we might represent documents. We are going to do a simple analysis of Shakespeare's plays, which are available in digital form from a USA library, the [Folger Shakespeare Library](https://www.folger.edu/explore/shakespeares-works/download/). We will look at the plain text of four plays:

- [As You Like It](https://flgr.sh/txtfssAYLtxt)
- [Twelfth Night](https://flgr.sh/txtfssTN_txt)
- [Julius Caesar](https://flgr.sh/txtfssJC_txt)
- [Henry V](https://flgr.sh/txtfssH5_txt)

**Practical**

- Each person will be allocated a play from the above list, and a word
- Count the number of times your word occurs in your play
- A simple way to do this is to use CTRL-F in your browser - this finds words in a page
- The dialog box in which you type the search word will tell you how many times that word occurs in the page
- Record your results in [this spreadsheet](https://docs.google.com/spreadsheets/d/1W-NI1-CAufuXTCHISsbwvnqY5krQVnsAxqX2IKpNcVg/edit?usp=sharing)

**Questions**

- *Wit* is also found in common words like *with* - how will you overcome this?
- Can we tell the difference between Shakespeare's comedies (e.g. As You Like It, Twelfth Night) and other plays?
- How might you represent a document?
- How might you visualise this?
- How might we use this document representation?
- Can you think of a waywe extend this to represent words?

## Representing words: vector semantics
[[back to top]](#top)

We've seen how to represent documents as vectors, but what about words themselves? 

**Presentation:**  This presentation introduces the idea of *distributional semantics*
- [Presentation: distributional semantics](./presentations/distributional-semantics.pdf) 

**Demonstration:** We will demonstrate the idea of using a word's context to create a vector representation of that word by using a linguistic search engine, [WebCorp](https://www.webcorp.org.uk/). WebCorp allows us to find and list all contexts on the web in which a word appears, and to count the number of times other words appear next to it. We call these the the word's collocates).
- [Demonstration: WebCorp](https://www.webcorp.org.uk/)

**Practical:** This practical builds word vectors using data from the [iWeb corpus](https://www.english-corpora.org/iweb/): a corpus of 14 billion words in 22 million systematically selected English language web pages. This can be searched and analysed using the tools at [English-Corpora.org](https://www.english-corpora.org/). We have used these tools to look at a few words, and to find what other words appear in their context. In this case, we define context as being on the same web page. We have saved the context counts in a spreadsheet, which has one sheet for each of our words:

- [Data: word contexts](./practicals/contexts.xlsx) (click the "View raw" button to download, tnen open on your computer)

You can use this spreadsheet with the Python notebook below to build and explore some word vectors:

- [Python notebook: vector semantics](https://githubtocolab.com/KCL-Health-NLP/nlp-one-day-workshop/blob/main/practicals/plot_contexts.ipynb)

## Playing with word embeddings
[[back to top]](#top)

The simple word and document vectors we built above can be used in NLP and information retrieval applications, but they have a few shortcomings, and better distributional semantics solutions exist: **word embeddings**. Whereas the vectors we have looked at so far are high dimensional with integer values, word embeddings are much lower dimensional (maybe a few hundred dimensions), with real number values. The most popular of these is Google's [Word2Vec](https://www.tensorflow.org/text/tutorials/word2vec) and Stanford University's [GloVe](https://nlp.stanford.edu/projects/glove/). We will use both of these in the practical below.

**Presentation:**
This presentation gives a high level, intuitive overview of word embeddings. For more details, and information on how they are built, see the links above and Chapter 6 in [Jurafsky and Martin](https://web.stanford.edu/~jurafsky/slp3/)
- [Presentation: word embeddings](./presentations/word-embeddings.pdf) 

**Practical:**
In this practical, you will create a word embedding from a small corpus and test it. It won't be very good! Then you will load an embedding that has been pre-trained on a much bigger corpus, to see the difference this makes.

- [Python notebook: word embeddings](https://githubtocolab.com/KCL-Health-NLP/nlp-one-day-workshop/blob/main/practicals/embeddings.ipynb)


## Supervised machine learning for simple text classification
[[back to top]](#top)

*Content in progress*

- [Presentation: supervised machine learning for text classification](./presentations/word-embeddingsclassification.pdf) 

- [Python notebook: classification](https://githubtocolab.com/KCL-Health-NLP/nlp-one-day-workshop/blob/main/practicals/classification.ipynb)


## Neural networks
[[back to top]](#top)

We now have some ideas of how we might represent words and language numerically, encoding some aspects of meaning. We could use these representations in the type of models you will have seen in the prediction modelling part of the Youth Awards. For example, you could build a model that takes document vectors of product reviews as input, and predicts whether the review is a positive or negative one. Or, you might take vectors representing medical record sentences and predict whether the sentence is about a particular symptom. 

Many modern NLP models make use of neural networks to do this kind of prediction. We will introduce and buid simple neural networks with a presentation and a couple of practials, and ask how might we use these with words and language? The practicals will model simple functions, rather than complex pieces of language.

**Presentation:**
In this presentation we introduce a single artificial neuron, called a perceptron. 
- [Presentation: a perceptron](./presentations/neural-networks.pdf) 

**Practical:**
In this practical, we build a perceptron in Python, use it to model some simple problems, and ask - what is the limit of it's representational power?
- [Python notebook: experiments with a single neuron](https://githubtocolab.com/KCL-Health-NLP/nlp-one-day-workshop/blob/main/practicals/perceptrons.ipynb)

**Presentation:**
In this presentaiton we look at how we can extend the power of our perceptron, by using multiple neurons:
- [Presentation: multi-layer neural networks](./presentations/multi-layer-neural-networks.pdf) 

**Practical:**
Let's play with a bigger network, to solve more complex problems:
- [Web site: neural network playground](https://playground.tensorflow.org/)


## Generative AI
[[back to top]](#top)

Now that we've got some idea of how neural networks work, we will look at some examples of more complex *transformer* networks as used in state-of-the-art NLP. These are the ones you see mentioned as generative AI in the news and have quite likley used yoursleves - ChatGPT and friends. We can't hope to go over all of the details, but will introduce some of the basic concepts and will run a model for you to play with.

**Presentation**
In this presentation we introduce the transformer architecture, and it's key component - the self-attention block. We will also talk about the output of these models - a probability distribution over a vocabulary.
- [Presentation: transformers and generative AI](./presentations/generative-models.pdf) 

**Practicals**
For the practicals, we will use Meta's Llama 3 large language mmodel. This is too big for you to comfortably donwload and install, so we will host it on a cloud platform run by an AI company, Hugging Face. In order to use the model, you will need to create a Hugging Face account. This is explained in the first practical: 

- [Python notebook: connecting to Hugging Face](https://githubtocolab.com/KCL-Health-NLP/nlp-one-day-workshop/blob/main/practicals/hugging_face.ipynb)

In the second practical, we explore a key concept in the use of large language models - writing questions to get back consistent and useful information from the LLM - this is *prompt engineering*. We will also look at how we might give the LLM examples of the kinds of answers we want - referred to as *few shot learning*.

- [Python notebook: experiments with Llama 3](https://githubtocolab.com/KCL-Health-NLP/nlp-one-day-workshop/blob/main/practicals/llama.ipynb)
