
# Teaching AI with p5js

Final project for the Building AI course

## Summary

I'm exploring ways to continue teaching some of the AI methods covered on the Building AI course in the classroom in an easy and creative way. 

## Background
p5.js is a JavaScript library for creative coding. With the p5.js web editor and machine learning library ml5js, it's possible to continue teaching many of the AI methods covered on the Building AI course to for example secondary school students, in a fun and engaging way. With p5.js, there's no need to install anything on the school computers, and the ease of writing code and creating nice graphics is a key element in keeping the students onboard. 
Instead of using ready-made, restricted examples, the students can use datasets of their own choice.

My personal motivation stems from my background in technology education and creative coding. 

## How is it used?

Target audience: secondary school students and their teachers. No prior understanding of programming needed. The learning materials must contain good code templates for younger students and novices.

The lesson plan will consist of at least these parts:
* introduction to creative coding with p5.js (coordinate system, drawing and colors, variables, mapping, functions, basic interactions, importing files, adding text) - 2 hours
* open data and data visualisation (concept of open data, examples of data types and sources, quick visualisations using Excel/Google Sheets, scatter plots on p5.js) - 2 hours
* linear regression (nice intro using some of the datasets: what is it, what can / can't you do with linear regression, what does it look like when visualised?) - 1h
* linear regression with p5.js and ml5js - 2h
* total: 7h

Classroom requirements:
* 1 computer / 2 students
* data projector + computer for the teacher
* solid internet connection

## Demo

I tested working with open data and Tensorflow.js tools. My test data was  to red and white variants of the Portuguese "Vinho Verde" wine. For more details, consult: [Web Link] or the reference [Cortez et al., 2009].

These datasets can be viewed as classification or regression tasks. The classes are ordered and not balanced (e.g. there are many more normal wines than excellent or poor ones). Outlier detection algorithms could be used to detect the few excellent or poor wines. Also, we are not sure if all input variables are relevant. So it could be interesting to test feature selection methods.


Data consists of these variables (based on physicochemical tests):
1 - fixed acidity
2 - volatile acidity
3 - citric acid
4 - residual sugar
5 - chlorides
6 - free sulfur dioxide
7 - total sulfur dioxide
8 - density
9 - pH
10 - sulphates
11 - alcohol
Output variable (based on sensory data):
12 - quality (score between 0 and 10)

After testing, I considered pH and alcohol percentage as good y and x values, and I used the quality as the color variable. Mapping of the data looks like this in p5.js:

![Wine Quality](/wine_mapping.png)
I made use of tutorials by Allison Parrish and Daniel Shiffman to create this demo (see Acknowledgements for details).

Direct link to the code:
https://editor.p5js.org/codingtrain/sketches/UtOWCSYYF

## Data sources and AI methods
https://archive.ics.uci.edu/ml/datasets/wine+quality
Paulo Cortez, University of Minho, Guimarães, Portugal, http://www3.dsi.uminho.pt/pcortez
A. Cerdeira, F. Almeida, T. Matos and J. Reis, Viticulture Commission of the Vinho Verde Region(CVRVV), Porto, Portugal

I'm investigating linear regression as the first method. 


## Challenges

Personally I'm struggling with TensorFlow.js, which I'm not familiar with. 
In the education setting it's important to sufficiently cover the technologies used, but it's equally crucial not to suffocate the students with too many new concepts. The balance with ready-made code and the students' own input requires careful design. 
If the students were to use datasets they find interesting, the data needs to be in the correct format, and it will take some effort to discuss what makes a useful dataset for linear regression what doesn't. T

## What next?
After I've made the code work, improving the lesson plans and testing them with students is a logical next step.
Linear regression is the first method I'm investigating, but it's likely that all the AI methods from Building AI can be taught on p5.js. 


## Acknowledgments

* P5js: https://p5js.org/
* Using csv data: https://creative-coding.decontextualize.com/csv-files/ by Allison Parrish
* Open datasets: https://lionbridge.ai/datasets/10-open-datasets-for-linear-regression/ 
* Code example on linear regression with p5.js and ml5js by Coding Train / Daniel Shiffman: https://thecodingtrain.com/CodingChallenges/104-linear-regression-tfjs.html

