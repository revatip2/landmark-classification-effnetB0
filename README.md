# Landmark Classification using EfficientNetB0

This repository contains code for a Landmark and Category Classification Model for Monuments using EfficientNetB0. The primary goal is to classify images into different categories and landmarks using machine learning techniques.

## Table of Contents

- [Introduction](#introduction)
- [Data Preparation](#data-preparation)
- [Model Architecture](#model-architecture)
- [Training](#training)
- [Evaluation](#evaluation)

## Introduction

In this project, we explore the use of the EfficientNetB0 model for image classification. The goal is to classify images into various categories and landmarks. The pipeline involves processes such as data loading, augmentation, preprocessing, model building, training, and evaluation.

## Data Preparation

The dataset consists of images categorized into different landmarks and categories. The images are loaded, preprocessed, and augmented using various techniques such as rotation, flipping, and noise addition.

## Model Architecture

The EfficientNetB0 model serves as the base architecture for image classification. The model includes custom layers and a dense classifier on top of the base model. Both category and landmark recognition are trained sequentially.

## Training

The model is trained using the training dataset, and the weights of the best-performing model are saved using checkpoints. The training involves fine-tuning the model layers and optimizing hyperparameters.

## Evaluation

The trained model is evaluated on validation and test datasets. Classification reports and confusion matrices provide insights into the model's performance for both categories and landmarks.

