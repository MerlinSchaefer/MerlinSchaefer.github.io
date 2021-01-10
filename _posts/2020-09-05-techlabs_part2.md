---
layout: post
title:  "Techlabs Berlin - Part Two: The Project Phase"
date: 2020-09-04 18:00:13 +0200
categories: Projects
---

berlinrents.live
====================

### Finding a Project

Throughout this summer I participated in the Techlabs Berlin Digital Shaper Program, which helped me built my skills in machine learning and AI. This is blog post is about the second part of the semester: the project phase.
After finishing the learning phase of Techlabs it was time for all students to put their newly acquired skills to work within group projects.
The projects were not just set projects for each track but came from us, students. Techlabs encouraged everybody to form ideas and come up with projects that would showcase the skills everyone had developed over the previous weeks.
After we had some time to develop ideas they were pitched at a small event, and submitted to the Techlabs-Team.
Everybody was asked to give a first, second, and third preference for the project they wanted to work on. Then the Techlabs-Team created the project teams.
I actually pitched an idea, but was so convinced by the pitch of two fellow students, that I chose to work on their idea instead of mine.

And so began the work on [berlinrents.live](https://drive.google.com/file/d/1R88lCPdal0uvbl1-JQneimi3uL7Mt173/view?usp=sharing).
(Click on the link to view our presentation Video)

### Defining the Problem

The first step in the process of realizing the project was to define the problem we aimed to solve and how our first "minimum-valuable-product" should look like.
We wanted to build a tool/website that would help people understand the current rental market in Berlin better. This included giving them as much useful information as possible and perhaps enabling them to see how rental prices had evolved over time.
We also wanted to make this data as current as possible, because existing tools and information were often over a year old.

### Team Tasks and Workflow

Our Team consisted of 4 people that had done the Data Science track, 1 person each from the WebDev and UX track, and me, coming from the AI track.
The Data Science team acquired all of the data via web-scraping, set up the backend of the web app, and created data visualizations.
Our Web Developer created the website our UX designer provided the logo and other important elements for the overall user experience.
I did some data exploration and data cleaning, which was needed anyway for my main task: building a machine learning model to estimate a rental price for a set of given features.

To coordinate our work we set up weekly virtual meetings and communicated via Slack. Our code was uploaded, shared, and reviewed through Github.
We also had a great project mentor, who gave us feedback and input whenever needed.

### Rental Price Estimation
#### Understanding the ML Problem & Exploring the Data
The problem at hand was a classic regression problem. I had some input features and needed a model that would produce a price estimate.
When you approach similar problems with data from e.g. Kaggle you usually have 10000+ rows and relatively clean data. This was not the case here.
We started with a few hundred rows of scraped rental offers and reached about 2500 offers at the end of the project phase. 
In different words: The dataset was very small for machine-learning standards, which of course posed a challenge.
More data is not always the silver bullet it is sometimes proclaimed to be, but a few thousand instances are often needed to produce a relatively accurate model.

The data also needed to be cleaned. In the beginning, all data was of the same type. That obviously needed changing. There were many outliers or just strange entries, such as rental offers for 0€ rent. Before training any model I had to deal with them.
Not all offers had appropriate geographical information which was needed for my model as well as the data visualizations. I, therefore, had to find a way to either map a postcode to every offer or find the latitude and longitude.
Some features such as balcony or cellar also had a lot of missings and more than 2 values. Unfortunately, we did not know the difference between kitchen = 2 and kitchen = 4. I tried to manually figure out what those numbers meant by manually going through the listings and comparing the offers to the features, but I could not figure out what the underlying logic was.
Every time I thought I spotted a pattern, I found counterexamples.
In the end, we found a system to make features such as cellar or kitchen availability binary.

#### Time to Play! - Trying out Machine Learning Models

After all of the data cleaning and preparation, the fun part could begin. Training models, selecting promising ones, tuning those, and finally combining them into an ensemble.

But not so fast..what about feature selection, you might ask.
I began working with a rather tiny dataset, which made it hard to perform any feature selection. Many correlations and other indicators for feature importance changed quite a bit every time new data came in.
I decided to start working on the models and perform the feature selection during the process, which sometimes made it hard to not overlook something and systematically try everything but in the end, it worked fairly well.

I kept the most important features such as apartment size and even two or three that did not make a difference. I kept these features because to a future user of the estimator, specifying only 3 or 4 parameters for a rental estimated probably would have seemed less credible, than specifying the features we would associate with higher rental prices such as having a balcony.

I explored many models for this regression task for example:
- OLS Linear Regression
- Ridge, Lasso, and Polynomial Regression
- SVMs
- Random Forest Regression
- a NN(200,100)
- Gradient Boosted Decision Trees

After a lot of testing and hyperparameter tuning a combination of the Ridge Regression, the Random Forest and the Gradient Boosted Decision Tree offered the best performance.

The model was trained and saved so that the Webpage could send the user-specified parameters and get a prediction from the already trained model.

This model however was still off by quite a large amount of money (on average). I, therefore, decided that providing a range instead of a point estimate to the user would be beneficial.
This does not only help to incorporate the model-error into the estimation but also avoids providing a false sense of accuracy to the users.

The result on the webpage looked like this:
![The Web Interface for the Price Estimation](/assets/images/berlinrents_estimate.png)
![The Web Interface for the Price Estimation](/assets/images/berlinrents_estimate2.png)

You can check out the whole Webpage [here](https://berlinrentslive.herokuapp.com/).

*Please note that it was not maintained after the project was submitted. Some things may not work correctly anymore. It is also hosted on a free web server, which brings some limitations, **you will probably have to load the webpage twice in the beginning.***

You can find a short presentation of our final project [here.](https://drive.google.com/file/d/1R88lCPdal0uvbl1-JQneimi3uL7Mt173/view?usp=sharing)

I later retrained the model from time to time and adjusted some of the data cleaning which lead to better performance. However, these changes are not in the current codebase for the webpage.

### My Personal Experience with the Project

I learned a lot during this project. It was my first time working with a team on a tech project.
I really enjoyed the experience and was fortunate to have smart and dedicated individuals working alongside me.

I wasn't able to directly built on or expand my newly gained knowledge about deep learning and neural networks which was a little unfortunate (and partly due to the fact, that the NN did not perform great).
I did, however, learn more about machine learning and regression problems in general. 
I was also able to practice my coding in that specific domain. 
I additionally got much more comfortable using Git and Github.

Overall it was a great (learning) experience and my first real project. I am happy with what I learned and produced, as well as how our project turned out.

-Merlin
