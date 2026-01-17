# Fooling Neural Networks with Optimization: Frank-Wolfe and PGD Methods in Machine Learning

## Introduction & Objective

Our goal is to explore the vulnerability of neural networks through the lens of mathematical optimization, specifically focusing on white-box adversarial attacks. To analyze model robustness, we implemented and compared several optimization strategies: from the standard Fast Gradient Sign Method (FGSM) to more advanced iterative techniques like Projected Gradient Descent (PGD) and various versions of the projection-free Frank-Wolfe algorithm (including momentum-based, away-step, and pairwise variants). 

The goal is to investigate how these different optimization behaviors affect the effectiveness of the attacks under $L_2$ and $L_\infty$ norm constraints. This helps us understand the trade-offs between projection-based and projection-free methods in terms of convergence and fooling ability. In the end, we tested these algorithms on the MNIST and ImageNet datasets, identifying the most appropriate perturbation ranges ($\epsilon$) and performing an exhaustive set of experiments to get a comprehensive analysis of each algorithm's effectiveness.

## Steps followed

To perform our analysis we followed these steps:
1. **Model & Data Setup:** Preparation of the MNIST CNN architecture and loading of pre-trained checkpoints.
2. **Algorithm Implementation:** Development of PGD and Frank-Wolfe optimization loops for adversarial generation.
3. **Experimental Evaluation:** Testing and interpretation of attack success rates across different datasets and constraints.
