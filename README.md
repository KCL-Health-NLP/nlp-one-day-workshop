# Natural Language Processing (NLP) - a one day introductory workshop
*A one day workshop on NLP with a health record focus prepared for [MQ Mental Health Research](https://www.mqmentalhealth.org/) and [DATAMIND](https://datamind.org.uk/) by [King's College London Institute of Psychiatry, Psychology and Neuroscience](https://www.kcl.ac.uk/ioppn)*

## Learning objectives

- Understand the need to process language when re-using electronic health records for research, the computational difficulties language poses, and how natural language processing (NLP) can help to solve these.
- Appreciate the main paradigms of NLP, and their relative strengths and weaknesses.
- Develop an overview of how language is represented computationally, and how these representations can be used to build models of text.
- Gain a basic understanding of neural networks, their use in NLP, and generative AI.
- Gain practical experience of building simple NLP applications using Python.
- Appreciate the broader health research context in which NLP can sit, and the development process needed to implement NLP in this context.


## Target audience and skills required

- The course is aimed at early career health researchers who want to explore the basic concepts of NLP and its application to electronic health record text.
- The course is not primarily aimed at those with an extensive computer science or data science background, though you are welcome to come along, and perhaps benefit from a different perspective.
- This is not a theoretical course, though we will provide pointers for further reading after the course.

## Format

The course will be delivered through:

- Pre-workshop video lectures and preparatory material.
- A one day hands-on practical workshop. This will mainly consist of Python practicals, interspersed with very short presentations.
- Suggested reading for those of you who want to explore the topic further.

## Pre-workshop material

You can find links to the introductory video lectures below. You should watch these before the workshop. The lectures are taken from a 10 day taught course on NLP, and on occasion refer to other parts of that course. Just ignore those references - you only need the main content of these lectures.

There are also links to some  introductory material on Python and machine learning for those of you who need it.

**NB To download the slides, click a slide link below, then click the 3 dots to the right of the window that opens, and choose download.**

#### Introduction to NLP for health research
These two lectures motivate the need for NLP of electronic health records (EHR), and give a high level overview of methods used.

- Motivation \[[Video lecture](https://media.kcl.ac.uk/media/Natural+language+processing+for+healthcare+-+motivation/1_meicypfl)\] \[[Slides](./pre-course-material/nlp-motivation.pdf)\]
- Methods \[[Video lecture](https://media.kcl.ac.uk/media/Natural+language+processing+for+healthcare+-+methods/1_vrghd605)\] \[[Slides](./pre-course-material/nlp-methods.pdf)\]

#### Modelling language
How can we represent language so that it can be processed computationally? Can we capture any of the semantics or meaning of language in our representations? These three video lectures introduce ways in which canwe might do this. In the workshop, we will use these methods, and extend them.

- Modelling documents \[[Video lecture](https://media.kcl.ac.uk/media/modelling-language-documents-video/1_fv1owosr)\] \[[Slides](./pre-course-material/modelling-language-documents.pdf)\]
- Modelling words \[[Video lecture](https://media.kcl.ac.uk/media/modelling-language-words-video/1_rc5qg9ti)\] \[[Slides](./pre-course-material/modelling-language-words.pdf)\]
- Distributed representations \[[Video lecture](https://media.kcl.ac.uk/media/modelling-language-distributed-video/1_3rxamdmd)\] \[[Slides](./pre-course-material/modelling-language-distributed.pdf)\]

#### Setting up clinical NLP studies
These two lectures look at the bigger picture: how does NLP of health records fit in to epidemiology and health research? With credit to Dr Sumithra Velupillai who contributed this material whilst working at King's College London.

- Setting up clinical NLP studies - Part A \[[Video lecture](https://media.kcl.ac.uk/media/SV1-NLP_Intro-steps_to_set_up_clinical_NLP_partA/1_ldeuexyq)\] \[[Slides](./pre-course-material/SV1-NLP_Intro-steps_to_set_up_clinical_NLP_partA.pptx)\]
- Setting up clinical NLP studies - Part B \[[Video lecture](https://media.kcl.ac.uk/media/SV1-NLP_Intro-steps_to_set_up_clinical_NLP_partB/1_q5z7kjso)\] \[[Slides](./pre-course-material/SV1-NLP_Intro-steps_to_set_up_clinical_NLP_partB.pptx)\]

#### Python

The workshop practicals will all be in Python. If you don't know much Python, don't worry - you don't need to write much code and we will provide fully worked answers. You should be able to step through the practicals and follow what is happening with some rudimentary Python skills, e.g. sufficient to read Python code. You will, however, get more out of the practicals if you have followed an introductory Python course covering basic syntax. Even better if you know a little about the pandas data handling package and scikit machine learning package.

There are some good [Datacamp Python courses](https://www.datacamp.com/category/python) - some of these are free. Includes intro courses, data analytics, pandas, scikit machine learning.

#### Introduction to Google Colab

We will use [Google Colaboratory](https://colab.google/), or "Colab" for the workshop practicals. Colab is a web-based Python environment. It has the advantage of not requiring you to install any software, and of us being able to provide a consistent environment for all workshop partipants. You will need a Google / Gmail account to use it. If you are not familiar with Colab, take a look at this [introduction from Google](https://colab.research.google.com/notebooks/basic_features_overview.ipynb) or this [this short practical](https://colab.research.google.com/github/angusroberts/asmhi-python/blob/master/01-using-colab.ipynb)

You are welcome to use different Python tools in the workshop, but we will not be able to help you solve any version or environment problems.

#### Machine learning

Although not essential, you will get more out of the workshop if you have some knowledge of machine learning. A good place to get a thorough introduction is the excellent [DATAMIND Machine Learning in Mental Health YouTube playlist](https://www.youtube.com/playlist?list=PLt7J6CW_cQg_lFKAnOYirgwM5qTB4jaGH). The first 8 videos will be the most useful, but the others are also relevant.


## Workshop - on-the-day agenda and contents

We will cover the following topics in the workshop, and will place links to the material here, for you to use on the day.

- Introduction
- Vector semantics and representing language
- Supervised machine learning for a simple text classification problem
- Word embeddings
- A single artificial neuron - the perceptron
- Building multi-layer neural networks
- A simple neural network for text classification
- Generative AI and prompt engineering

## Further reading

We will provide a reading list of further material after the workshop, for those of you who want to explore the topic further.
