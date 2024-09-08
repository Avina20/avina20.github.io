---
layout: page
title: Classmate.io
description: Revolutionizing learning experience using gamification and AI; Web app built on AWS using NLP techniques 
img: assets/img/elearning.jpg
importance: 1
category: work
related_publications: true
---

In response to the challenges posed by digital distractions in contemporary education, this study introduces a scalable web application designed to revolutionize the learning experience. Traditional learning methods, reliant on note-taking and memorization, often struggle to captivate students in an era of abundant internet-based diversions. The proposed solution addresses this issue by incorporating gamification principles, offering a reward system and feedback analysis to boost engagement and motivation. Beyond typical Multiple-Choice Question (MCQ) generation, the application encompasses features such as text summarization, notes handling, login/signup functionality, lecture transcription, and efficient data storage. By providing a multifaceted approach to learning enhancement, the web application seeks to create a conducive environment for students who grapple with distractions. All while building a scalable application on Cloud and incorporating MLOPs features!

    ● MCQ Generation
    ● Text Summarization
    ● Notes Handling
    ● Log In & Sign Up
    ● Transcription of Lectures
    ● Efficient storage of data objects.
    ● Event tracking

<div class="row justify-content-sm-center">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/nlp.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/mlops.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


The architecture of our application revolves around seamlessly managing student notes, employing various functionalities for a comprehensive learning experience. A seamless Machine Learning Ops system which has the components of data pipelines, automatic model training, and model deployment using the AWS `Sagemaker`.Leveraging AWS `Lambda`, our application handles diverse tasks such as note creation, summarization, updating, and deletion using CRUD. By integrating `S3` for efficient storage and retrieval of notes, Amazon `Transcribe` for audio lecture transcription, the application ensures a robust and scalable infrastructure. Through API `Gateway`, we facilitate secure communication between clients and Lambda functions, ensuring data integrity and confidentiality. The application employs AWS `Cognito` for user authentication, enhancing security. We deployed our Flask application on Amazon `EC2`, a virtual server service offered by AWS that allows us to launch virtual servers in the cloud, with varying CPU, memory, storage, and networking capacity. AWS `Lex` for the implementation of a chatbot for website navigation, `DynamoDB` for data storage and `SNS` for event alerts

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/classmateIo.png" title="example image" class="img-fluid rounded z-depth-1"%}
    </div>
</div>
<div class="caption">
    Architecture diagram
</div>

`TEXT SUMMARIZATION`

In our project, we have utilized the DistilBart-CNN-12-6 model and fine-tuned it on the Cornell
arxiv dataset which contains paper abstracts and their respective titles. Data Source and Model data have been stored in the default AWS sagemaker bucket for our Studio and Instance Configuration were set to use Python 3.9 with Pytorch v1.13 and a server type of ml.p3.2xlarge
which utilized 8 vCPUs, 61 gb of instance memory and 1 Nvidia v100 GPU. Then, AWS Sagemaker creates a Training job and retrieves and provisions the respective Deep Learning Container image onto our instance and runs the training.


`MCQ GENERATION`

`Keyword Extraction` - Named Entity Recognition or Noun chunk extraction is applied on every selected sentence and to select the word which is important
`NAMED ENTITY RECOGNITION` - Named entity recognition (NER) helps in the process of information extraction that locates and classifies named entities in text into predefined categories
`DISTRACTOR GENERATOR`-Distractor generator is made with the purpose to distract the students from the correct answer choice. The extracted keywords are fed into models trained by Gensim and
Word2Vec embeddings in order to generate similar words.
`GENSIM` - Gensim is a Python library for topic modeling, document indexing and similarity retrieval with large corpora.
`WORD2VEC` - Word2Vec is one of the most popular techniques to learn word embeddings using shallow neural networks. Word embedding is one of the most popular representations of document vocabulary.
`GLOVE` - Unsupervised learning algorithm for vectorization of words from a corpus which we have used in our Training.

The code for the web app can be found here : <a href="https://github.com/Avina20/classmate-io">Code</a>

Additional code for NLP implementations for text summarization and improved MCQ generation can be found here <a href="https://github.com/Avina20/MCQ-generator">Here</a>