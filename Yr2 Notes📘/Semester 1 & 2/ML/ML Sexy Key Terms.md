---
tags:
  - machine
  - learning
  - revision
  - obsidian
  - CM22009
  - glossary
title: Machine Learning Y2425-CM22009 Key Terms
---
# ML Sexy Key Terms
---
> [!info]+ File Details
> Includes information about this (genus:: Note) from [Year::2]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  14-04-2025
> > *Module :* [[Machine Learning]]
> > *Teacher*: #Chatted 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> > [[#Speed run]]
> [[#🧮 Definitions by Topic]]
> [[#]]
> [[#]]
> [[#]]

--- 
> [!danger]+ *Speed run*
> - **Optimisation**: Gradient Descent, Stochastic Gradient Descent, Momentum, Nesterov Accelerated Gradient, Adam Optimizer, Learning Rate, Convexity, Hessian Matrix  
> - **Supervised Learning**: Supervised Learning, Regression, Classification, Multivariate Regression, Binary Classification, Multiclass Classification, Overfitting, Generalization, Loss Function, Cross-Entropy, Squared Error Loss, Maximum Likelihood Estimation, Negative Log-Likelihood  
> - **Unsupervised Learning**: Unsupervised Learning, Clustering, K-means Clustering, DBSCAN, Hierarchical Clustering, Gaussian Mixture Models, Expectation-Maximization  
> - **Dimensionality Reduction**: Principal Component Analysis, Singular Value Decomposition, Covariance Matrix, Whitening  
> - **Generative Models**: Generative Models, Latent Variables, Gaussian Mixture Models, EM Algorithm, Variational Inference  
> - **Neural Networks**: Shallow Neural Network, Deep Neural Network, Feedforward Network, Activation Function, Sigmoid, ReLU, Tanh, Bias Node, Forward Pass, Backward Pass, Backpropagation, Chain Rule  
> - **Neural Network Variants**: CNN, Pooling Layer, Dilation, RNN, LSTM, Skip Connection, Residual Block, Identity Shortcut, Vanishing Gradient, Exploding Gradient  
> - **Regularisation Techniques**: Regularisation, L1, L2, Elastic Net, Dropout, Early Stopping, Checkpointing, Data Augmentation  
> - **Loss & Evaluation**: Loss Curve, Validation Data, Training Data, Underfitting, Hallucination, Empirical Distribution, Model Distribution, KL Divergence, Entropy  
> - **NLP & Language Models**: NLP, NLU, NLG, Language Model, Transformer, Masked Language Model, Pretraining, Fine-tuning, Back-Translation, Chain-of-Thought Prompting, Self-Consistency Prompting, Emergent Behavior, AI-Hard, Hallucination

---


> [!heart]+ Exam Format
> ![[ML Exam Format.png]]
> ![[MLexamSupervised.png]]
> ![[MLexamUnsupervised.png]]

---
## 🧮 Definitions by Topic

> [!abstract]+ Optimisation
> - **[Gradient Descent](https://en.wikipedia.org/wiki/Gradient_descent)**: Iterative method to minimize loss by moving in the direction of steepest descent.
> - **[Stochastic Gradient Descent](https://en.wikipedia.org/wiki/Stochastic_gradient_descent)**: Variant of gradient descent using one or few samples per update for faster convergence.
> - **[Momentum](https://en.wikipedia.org/wiki/Stochastic_gradient_descent#Momentum)**: Improves SGD by considering previous gradients to accelerate convergence.
> - **[Nesterov Accelerated Gradient](https://towardsdatascience.com/nesterov-accelerated-gradient-how-it-works-7cb5bbb597b2)**: Looks ahead to future positions to adjust updates more precisely.
> - **[Adam Optimizer](https://arxiv.org/abs/1412.6980)**: Combines momentum and adaptive learning rates.
> - **[Learning Rate](https://machinelearningmastery.com/learning-rate-for-deep-learning-neural-networks/)**: Controls step size in updates.
> - **[Convexity](https://en.wikipedia.org/wiki/Convex_function)**: A convex loss function ensures a single global minimum.
> - **[Hessian Matrix](https://en.wikipedia.org/wiki/Hessian_matrix)**: Second-order derivative matrix used in optimization.

> [!tip]+ Supervised Learning
> - **Supervised Learning**: Learning from labeled data to map inputs to outputs.
> - **Regression**: Predicting continuous outputs.
> - **Classification**: Predicting discrete classes.
> - **Multivariate Regression**: Predicting multiple dependent variables.
> - **Binary Classification**: Two class decision-making task.
> - **Multiclass Classification**: Classification with more than two classes.
> - **Overfitting**: When a model memorizes training data and performs poorly on unseen data.
> - **Generalization**: Model’s ability to perform well on new, unseen data.
> - **Loss Function**: A function that measures prediction error.
> - **Cross-Entropy**: A loss function used for classification problems.
> - **Squared Error Loss**: Used in regression to penalize the square of errors.
> - **Maximum Likelihood Estimation (MLE)**: Estimates parameters by maximizing data likelihood $\mathcal{L}(\theta) = P(D|\theta)$; training often minimizes $-\log \mathcal{L}(\theta)$ as loss.
> - **Negative Log-Likelihood**: Inverse of MLE, minimized during training.

> [!info]+ Unsupervised Learning
> - **Clustering**: Grouping data based on similarity.
> - **K-means**: Iterative centroid-based clustering.
> - **DBSCAN**: Density-based clustering that handles noise.
> - **Hierarchical Clustering**: Builds nested clusters either bottom-up or top-down.
> - **[Gaussian Mixture Models (GMM)](https://en.wikipedia.org/wiki/Mixture_model)**: Probabilistic model assuming data comes from Gaussian distributions.
> - **EM Algorithm**: Optimizes models with latent variables using Expectation and Maximization steps.

> [!success]+ Dimensionality Reduction
> - **[PCA](https://en.wikipedia.org/wiki/Principal_component_analysis)**: Reduces dimensionality by projecting data onto principal components. This is done by finding directions of maximum variance via eigen-decomposition: $\Sigma = \frac{1}{n} X^T X$.
> - **[SVD](https://en.wikipedia.org/wiki/Singular_value_decomposition)**: Factorizes a matrix $A = U \Sigma V^T$ into three components to analyze data structure.
> - **Covariance Matrix**: Captures linear relationships between features.
> - **Whitening**: Transforms features to have zero mean and unit variance.

> [!heart]+ Neural Networks
> - **Feedforward NN**: Neural net where connections do not form cycles.
> - **ReLU/Sigmoid/Tanh**: Nonlinear activation functions.
> - **ReLU**: $f(x) = \max(0, x)$
> - **Sigmoid**: $\sigma(x) = \frac{1}{1 + e^{-x}}$
> - **Tanh**: $\tanh(x) = \frac{e^x - e^{-x}}{e^x + e^{-x}}$
> - **Backpropagation**: Training algorithm using gradient descent.
> - **Bias Node**: Allows output without input activation.
> - **Forward Pass**: Data propagates through the network.
> - **Backward Pass**: Gradients propagate for parameter updates.

> [!bug]+ Neural Network Variants
> - **CNN**: Neural networks using convolutions for spatial data.
> - **Pooling Layer**: Downsamples features to reduce dimensionality.
> - **RNN**: Processes sequences by passing hidden states.
> - **LSTM**: Enhanced RNN with gates to manage memory.
> - **Skip Connection**: Shortcut paths to mitigate gradient issues.
> - **Identity Shortcut**: Simple skip connection using $( x + F(x) )$.

> [!warning]+ Regularisation
> Regularisation reduces overfitting and improves generalisation. explicit penalises model complexity and Implicit refers to regularisation affects that appear naturally in the process
> - **L1 (Lasso)**: Promotes sparsity in weights. $penalty = p + \lambda \times |Weight \ size|$
> - **L2 (Ridge)**: Penalizes large weights. $penalty = p + \lambda \times Weight \ size^2$
> - **Elastic Net**: Combines L1 and L2.
> - **Dropout**: Randomly disables neurons during training.
> - **Early Stopping**: Halts training when validation loss increases.
> - **Checkpointing**: Saves model state periodically.
> - **Data Augmentation**: Increases data diversity using transformations.

> [!omega]+ NLP & Language Models
> - [Transformers](https://en.wikipedia.org/wiki/Transformer_(machine_learning_model)) compute self-attention: $\text{Attention}(Q, K, V) = \text{softmax}\left(\frac{QK^T}{\sqrt{d_k}}\right)V$.
> - **[NLP](https://en.wikipedia.org/wiki/Natural_language_processing)**: Processing and understanding natural language.
> - **NLU/NLG**: Subfields of NLP for comprehension and generation.
> - **Transformer**: Deep learning model using attention mechanisms.
> - **[Masked Language Modeling (MLM)](https://huggingface.co/transformers/glossary.html#masked-language-modeling)**: Predicts masked words for pretraining (used in BERT).
> - **Back-Translation**: Re-translation for quality check or augmentation.
> - **Emergent Behavior**: Unexpected capabilities in large LMs.
> - **Hallucination**: Confident but factually incorrect output.


> [!flower] Miscellaneous
> ML lifecycle ![[ML lifecycle.png]]
> 