# Research - Machine grader

## Overview of [Zion's thesis](https://scholarship.rice.edu/handle/1911/111179)

| Structure                                                    |
| ------------------------------------------------------------ |
| Stage 1: Student code -> Python object                       |
| Stage 2: Python object -> Chart model representation (converter) |
| Stage 3: Compare with the expected result (grader)           |

**Universal Chart Model**

- In the Universal Chart Model (UCM, or simply the chart model), a chart consists of a hierarchical collection of components that we refer to as elements. These elements have associated types that determine their possible attributes. We implement them as nested dictionaries and visualize them as concentric boxes.
- An instance of the UCM for a particular chart is always a tree.

**Universal Chart Specification**

- The Universal Chart Specification (UCS, or simply the chart spec) inductively defines the correctness of the student’s chart model with respect to the instructor’s chart model.

**Future work**

- Integrating cross-layer information. 
- Automatic conversion.
- Designing a new plotting package.

**Inspiration by Zion**

- As matplotlib/plotly objects are trees, we can develop machine learning algorithms to learn the features of trees. This is a kind of cross-layer information.
- Our machine learning algorithms for the machine grader should be explainable and able to give students feedback. Otherwise, it will not help students have a better learning experience. 

## My thoughts

**Research objectives**

- Design explainable machine learning algorithms that provide cross-layer information to the machine grader.
- Let our ML-based machine grader be able to give students readable feedback.

**System model**

We can compare students' objects and instructors' objects by some graph comparison algorithms, such as graph kernels used to measure similarities between graphs. The figure below is from [a review paper](https://www.researchgate.net/publication/262524340_Graph_Matching_and_Learning_in_Pattern_Recognition_in_the_Last_10_Years) written in 2014. 

<img src="https://cdn.mathpix.com/snip/images/c4JSf2aSfzwYPgFwajk2GbjF54E0mTOjvyKtVnLeFjY.original.fullsize.png" style="zoom:25%;" />

**Difficulties**

Difficulty 1: We do not have tons of data.

Solution:

 - We can use traditional methods for ML on graphs. They need less data than deep learning.
 - We can try to learn with fewer labeled examples with skills including:
    - Data augmentation
    - Transfer learning
    - Semi-supervised learning
    - Active learning
    - Meta-learning
    - Few-shot learning
    - Weakly supervised learning

Difficulty 2: The machine learning model should show how students can improve their plots.

Solution: 

- By using explainable ML algorithms, we should be able to tell students how to improve their plots.

Difficulty 3: If our model makes wrong predictions, it might be misleading.

Solution:

- Give a probability score and let students trust themselves.

**Pros**

- Provide cross-layer information to the machine grader.
- Perhaps we do not need conversion anymore, and the machine grader can be generalized to all plotting packages as they all generate tree-structure objects.
- We do not need to manually design the machine grader if we have new projects.

**Cons**

- I don't think our machine learning model will outperform Zion's machine grader in accuracy, but let us see.
