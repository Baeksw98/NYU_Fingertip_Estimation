# Fingertips Position Estimation of a Robot Hand using 3D Images

Author: Sangwon Baek  
Institution: Center for Data Science, New York University  
Course: DS-UA 471: Intro to Machine Learning 
Professor: Lerrel Pinto 

## Overview

This project focuses on estimating the position of robot hand fingertips using 3D images, a challenging task in computer vision. The primary goal was to minimize the root mean squared error (RMSE) on unseen data, achieving a highly precise model with an RMSE of 0.00222.

## Table of Contents

- [Data Loading & Transformation](#Data-Loading-&-Transformation)
- [Modeling Architecture](#Modeling-Architecture)
- [Optimizer & Learning Rate](#Optimizer-&-Learning-Rate)
- [Model Training & Early Stopping](#Model-Training-&-Early-Stopping)
- [Experimental Results](#Experimental-Results)
- [Discussion](#Discussion)
- [Future Work](#Future-Work)

## Data Loading & Transformation

The image dataset was loaded using a lazy loading class to optimize memory usage. It involved preprocessing steps like normalizing RGB and depth images and resizing for better prediction accuracy.

## Modeling Architecture

Transfer learning of pretrained models on ImageNet was implemented, with ResNet-152 chosen as the primary model. Modifications were made to the ResNet architecture to fit the specific requirements of fingertip position estimation.

## Optimizer & Learning Rate

The Adam optimizer with a learning rate of 1e-3 was found to be the most effective. The model also utilized the StepLR learning rate scheduler to fine-tune the training process.

## Model Training & Early Stopping

The dataset was divided into training and validation sets (8:2 ratio). Early stopping was implemented to prevent overfitting, with the patience parameter set to 5 epochs.

## Experimental Results

Quantitative performance was assessed for various image combinations, aiming to achieve the lowest RMSE scores.

## Discussion

The project involved exploring different hyperparameter combinations and data preprocessing techniques. However, certain data augmentation methods like rotation and flipping were found unsuitable due to their adverse impact on RMSE scores.

## Future Work

Potential future directions include exploring new state-of-the-art models, fine-tuning hyperparameters, and applying advanced normalization and transformation techniques. A follow-up project may explore methodologies related to hand pose estimation using 2D/3D ground truth heatmaps.
