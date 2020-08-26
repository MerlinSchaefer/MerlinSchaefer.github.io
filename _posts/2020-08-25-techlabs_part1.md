---
layout: post
title:  "Techlabs Berlin - Part One: The AI track"
date: 2020-08-25 18:00:13 +0200
categories: Courses
---

Techlabs Berlin
====================

At the beginning of this summer, I received an email through the newsletter of the psychology faculty at my university.
It talked about a "Digital Shaper Program" that aimed to provide individuals with knowledge in tech-subjects such as WebDev or Data Science. It was free, offered the opportunity to learn and expand my skills, and most importantly to connect with like-minded individuals (something I wasn't really able to do before, as I had only taken online courses). 
Naturally, I was interested so I visited the [Program-Website](https://www.techlabs.org/program/local).
[Techlabs-Berlin](https://bln.techlabs.org/media) also provided a few videos, with information about the different tracks (e.g. WebDev, Data Science) and the general outline of the project.

The whole program was split into two major parts:
- a couple of weeks of self-paced (within the given timeframe) learning in the chosen track
- a project phase, which let individuals from different tracks team-up to work on and deliver a tech product

Throughout that time multiple social and "learning" events took place as well.

I was intrigued and applied to take part in the summer semester.
After being accepted I had to choose a track for the learning phase, which I will cover in this post.

## The AI track

At first, I wanted to choose the Data Science track, as the AI track was the only one that required previous knowledge. I was unsure if the skills I had gathered through self-studies and Courses such as the [Machine-Learning](https://merlinschaefer.github.io/courses/2020/06/09/ng_mlcourse.html) Course by Andrew Ng and the Data Science Specialization from the UoM, would suffice.

However, I wanted to challenge myself and avoid spending a lot of time on learning skills I had already required. After a short chat with the AI track leader, I decided to go for the AI track. 
In hindsight, this was a good decision. I learned a lot, in one of the areas that I was still lacking knowledge in, Deep Learning and Deep Neural Networks (NNs).

## The Learning phase

The teaching/self-learning happened on a platform called edyoucated, which held all the relevant material, curated by Techlabs, for the AI track as well as for other topics in case one wanted to broaden ones understanding of all things "tech".

The Platform was linked to different resources, such as Videos, parts of online courses, papers, and little exercises/challenges. For the completion of every task/material points were awarded, which increased the sense of progress and accomplishment.
The AI track consisted mainly of the [fast.ai](https://www.fast.ai/) course on deep learning, which gave an excellent hands-on, top-down introduction to many topics, such as computer vision and NLP. It utilized the fast.ai library for Python, which made deep learning and related tasks very easy and didn't require as many steps as the same tasks using for example TensorFlow.
I can only recommend the fast.ai course, for anyone interested in deep learning, Jeremy Howard is a terrific instructor and his enthusiasm and "let's try it" attitude are contagious.

After the completion of the top-down fast.ai lecture about a topic, such as Convolutional Neural Networks (CNNs), the edyoucated platform led to a more bottom-up approach that explained the finer details of the deep networks and the algorithms behind the learning.
This information came mostly from the Deep Learning courses by Andrew Ng, which are taught in a similarly comprehensive manner as the Machine Learning course.

For even deeper understanding there were usually 1-2 scientific papers (as optional reading) for any topic. These were challenging at times but often gave a very deep look into the respective topics, such as ResNets.

The topic I most enjoyed within all courses was computer vision. I find it fascinating how a string of mathematical operations like convolutions or matrix multiplications can lead to an astonishing ability to "see".

The edyoucated track and Jeremy Howard encourage you to take your new knowledge and apply it to whatever you find interesting. As an exercise, I tried to use the fast.ai knowledge and framework to apply ResNets (ResNet34 and ResNet50) to the recognition of facial expressions of kids. I still had a dataset of kids, showing various facial expressions from a research project I did during my studies at the university. I prepared the data and led it through the deep learning pipeline, quite similar to how it is shown in the fast.ai course. 
My results were not nearly as good as all the other image classifiers I had tried out within the course. My classifier did very well on many emotions, but some such as surprise and fear were mixed up quite often.
I then investigated existing research and realized, that I had tackled a rather hard task. I also did not have vast amounts of data. After some research, I found a paper that used the  same dataset. The researchers reported better results, but not vastly better ones. They had used facial landmarks in addition to the raw images to help guide the Neural Net in distinguishing the different facial expressions.
Although my results were far from groundbreaking, I learned a lot. I aim to use similar techniques for more classification tasks, which hopefully lead to even better results.

I could go on and on about the topics and my learnings from the track and the underlying courses, but I won't. If you are interested in knowing more, check out the courses or go to the topic list at the end of the blog post and look into them. I promise you, it's worth it.

### My Personal Experience with the course

As I already mentioned, I learned a lot. I can use the fast.ai library to create some state-of-the-art deep learning models, for various tasks. I was also encouraged to invest time into learning more complex frameworks for theses tasks, such as PyTorch or TensorFlow/Keras. I found out that I like computer vision a lot. I learned about the inner workings of deep NNs, which also gave me a stronger appreciation of the math behind NNs. Of course, there is much more to learn within the field, and I aim to do just that. However, I now feel confident in using deep learning as a tool in future projects. 
One such project followed immediately after the Learning Phase of Techlabs. I will talk about it more in the next post.
The fact that all learning was self-paced, and that I did it while completing my last semester in my bachelor’s degree, as well as writing my thesis, also gave me more practice in time-management, task prioritization, and learning.

#### Topics covered in the AI track

- NNs and Deep Learning overview
- Image Classification and Segmentation
- Training NNs
- Theory behind CNNs
- Object Detection
- NLP
- Collaborative filtering, Embeddings
- RNNs
- Generative (adversarial) Networks
- ML Strategy


-Merlin