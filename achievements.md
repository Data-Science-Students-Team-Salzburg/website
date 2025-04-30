---
layout: default
title: Achievements
---
# Achievements

Here are listed the data science challenges we participated in as a 
team.

---
<br>

## **Autoimmune Disease Machine Learning Challenge**  
> **by Eric and Wendy Schmidt Center at the Broad Institute, USA**  
> *Part 1: Oktober 2024 – February 2025*
> 
> *Part 2: November 2024 – March 2025*
> 
> *Part 3: December 2024 – April 2025*

![Python](https://img.shields.io/badge/Python-yellow?style=flat&logo=python&logoColor=white) 
![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C?style=flat&logo=pytorch&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-%23F9AB00?style=flat&logo=googlecolab&logoColor=white)

### Part 1: 🏆 **2th Place / 75 submissions / 7800 participants – 2400$ Prize**
### Part 2: 🏆 **6th Place / 11 submissions / 8200 participants – 700$ Prize**
### Part 3: 🏆 still ongoing

[Learn more about the challenge](https://drive.google.com/file/d/1h5Z6euEbMD-8r0hSZsMEYEG-pb_nyiiH/view?usp=sharing)

**Overview**  
Autoimmune diseases occur when the immune system mistakenly attacks healthy 
cells, disrupting the body’s natural defense mechanisms. These diseases affect 
50 million people in the U.S., with cases rising globally.
One of the most prevalent autoimmune diseases is inflammatory bowel disease 
(IBD). To better understand and treat IBD, researchers sequence the RNA 
(transcriptome) of individual affected cells. However, this process is highly 
complex and expensive, making a predictive model for transcriptomics a valuable
tool in advancing research.
This challenge consisted of three independent sub-challenges, each addressing a
distinct aspect of this broader research problem:
- The task of Part 1 of this challenge was to 
  create a model that can deliver this expensive and hard to obtain 
  information from readily available pathology images.
- The task of Part 2 was to predict all genes of a cell from a (predicted) 
  subpart.
- The task of Part 3 was to rank all genes based on their ability to 
  distinguish between normal cells and ones showing dysplasia. 

**Approach**  
For task 1, we used the ResNet50 model implemented in PyTorch to directly  
map from the input images to the 460 genes (end-to-end deep learning approach).

For task 2, we took our trained ResNet50 model and its predictions, which 
served as the input to a standard neural network, which mapped from the 460 
predicted genes to all genes of the cell.

For task 3, we submitted many different approaches. Notable examples include
(i) determining the AUC value for all features, and sorting them according to 
that, and (ii) predicting the cells with dysplasia with the help of a neural 
network model, for which we extracted feature importances with the 
Integrated Gradients method from the Captum library. Integrated Gradients is 
a feature importance algorithm for neural networks.

