# Project 15 - Deep neural networks

## Learning objectives

1. Understand the mathematical foundation of deep neural networks.

    **My work:** By reading [Book - Probabilistic Machine Learning: An Introduction](https://probml.github.io/pml-book/book1.html) and [Book - Deep Learning](https://www.deeplearningbook.org/), I can write a concise and comprehensive class note to help students understand how DNNs work. This semester I am taking COMP 540, so I think I can be familiar enough with the knowledge before this summer.

2. Implement neural network models in Python.

    **My work:** The assignments in [CS231n](http://cs231n.stanford.edu/) are helpful. We can take their valuable parts, revise them, and design an assignment suitable for our class. Students will be required to develop modular neural network models with objective-oriented programming. 

3. Practice tuning parameters and generating plots that reflect the performances of the model.

    **My work:** I can write code to visualize the decision boundaries for 2-dimensional data and make plots for the convergence of the epoch accuracy. Also, I can generate the confusion matrix for the trained model.

4. Visualize the architecture of neural network models in Plotly (not sure which package is the best, maybe we will try other packages).

    **My work:** The [TensorFlow playground](https://github.com/tensorflow/playground) is open-sourced. It is an interactive visualization of neural networks, written in TypeScript using d3.js. However, the playground visualization is limited. For example, its maximum number of hidden layers is six, and it cannot customize the visualization, such as modifying the names of layers or accomplishing a more complex architecture. Another visualization tool, [TensorBoard](https://www.tensorflow.org/tensorboard), also does not support a customized layout. Therefore, I want to make a more generalized and customizable tool to visualize neural networks. Specifically, I make visualizations of DNNs as directed acyclic graphs.

## Project overview

This week's project focuses on building deep neural networks (DNNs). In this week's project, you will first develop a modular, fully connected neural network model and test it on the CIFAR-10 problem. Then, you will build a three-layer convolutional neural network model and test it on the same CIFAR-10 problem. You will also make visualizations for the performance and architecture of the DNNs. 

[Project 15 notebook](https://colab.research.google.com/drive/1a_FHvCIz3MBesGHAdvuYSGDXBfHUJDfb)
