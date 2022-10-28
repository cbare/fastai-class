# Notes from FastAI Class 2022

## Lesson 1: Getting started

[Lesson 1][l1] summary: FastAI Library. Bird or not bird image classifier.

Library for setting up a Ubuntu machine: [fastsetup][l1-4]

[fastai: A Layered API for Deep Learning][l1-5] by Jeremy Howard, Sylvain Gugger

[Tanishq Abraham's tutorial on Gradio + HuggingFace Spaces][l1-6]

Assignment: [NZ bird classifier](./notebooks/fastai-homework-1.ipynb).

[l1]: https://course.fast.ai/Lessons/lesson1.html
[l1-4]: https://github.com/fastai/fastsetup
[l1-5]: https://arxiv.org/abs/2002.04688
[l1-6]: https://tmabraham.github.io/blog/gradio_hf_spaces_tutorial


## Lesson 2: Deployment

[Lesson 2][l2] summary: deployment to Hugging Face Space with Gradio.

- [Gradio tutorial][gradio-tut] from @ilovescience
- [HF Spaces][hfs]
- Installing a python environment:
  - [fastsetup](https://github.com/fastai/fastsetup)
  - Windows: [WSL][WSL] and [Terminal][term]
- tinypets [github](https://github.com/fastai/tinypets) / [site](https://fastai.github.io/tinypets/)
- tinypets fork [github](https://github.com/jph00/tinypets) / [site](https://jph00.github.io/tinypets/)

Assignment: [Deploy NZ bird classifier to Hugging Face](https://huggingface.co/spaces/christopherbare/nz-bird-classifier).

[l2]: https://course.fast.ai/Lessons/lesson2.html
[gradio-tut]: https://tmabraham.github.io/blog/gradio_hf_spaces_tutorial
[hfs]: https://huggingface.co/spaces
[WSL]: https://docs.microsoft.com/en-us/windows/wsl/install
[term]: https://apps.microsoft.com/store/detail/windows-terminal/9N0DX20HK701


## Lesson 3: Neural net foundations

[Lesson 3][l3] summary: Demonstrate gradient descent by fitting a quadratic. Introduce ReLUs.

What about the trade-off between inference time and performance? Here's a notebook that tries to answer that question: [Which image models are best?][models]

Side notes: An alternative to Kaggle notebooks, Colab, etc. is [Paperspace Gradient Notebooks][ps]. IPYWidgets [interact][interact].

[models]: https://www.kaggle.com/code/jhoward/which-image-models-are-best
[ps]: https://www.paperspace.com/gradient/notebooks
[interact]: https://ipywidgets.readthedocs.io/en/stable/examples/Using%20Interact.html
[l3]: https://course.fast.ai/Lessons/lesson3.html


## Lesson 4: Natural Language (NLP)

[Lesson 4][l4] summary: Introduction to NLP using [Hugging Face Transformers][hftransf] and the notebook [Getting started with NLP for absolute beginners][nlpnb]. Overfitting and underfitting. Metrics, correlation. Bot comments to the FCC on Net Neutrality.

Why does transfer learning work? When we fine-tune a pretrained model, we're making use of the low level features already learned in the pretrained model. [Visualizing and Understanding Convolutional Networks][viscnn] by Matthew D Zeiler, Rob Fergus.

NLP workflow: tokenization -> numericalization -> modeling.

[The problem with metrics is a big problem for AI][metrics].
[Creating a good validation set][val]

### Side notes

- [Python for Data Analysis][p4da], 3ed. Wes McKinney

[nlpnb]: https://www.kaggle.com/code/jhoward/getting-started-with-nlp-for-absolute-beginners
[hftransf]: https://huggingface.co/docs/transformers/index
[viscnn]: https://arxiv.org/abs/1311.2901
[p4da]: https://wesmckinney.com/book/
[l4]: https://course.fast.ai/Lessons/lesson4.html
[metrics]: https://www.fast.ai/posts/2019-09-24-metrics.html
[bots]: https://medium.com/hackernoon/more-than-a-million-pro-repeal-net-neutrality-comments-were-likely-faked-e9f0e3ed36a6
[val]: https://www.fast.ai/posts/2017-11-13-validation-sets.html


## Lesson 5: From-scratch model

[Lesson 5][l5] summary: Using the Titanic dataset, build a [linear model and neural net from scratch][fromScratch].

Feature engineering:

- missing data
  - mode imputation
  - introducing categorical variables to indicate missingness.
- taking the log of variables with long-tailed distributions
- creating one-hots to represent categories
- processing names to discover families and more
- normalization

[fromScratch]: https://www.kaggle.com/code/jhoward/linear-model-and-neural-net-from-scratch
[l5]: https://course.fast.ai/Lessons/lesson5.html


## Lesson 6: From-scratch model

[Lesson 6][l6] summary: Random forests, gradient boosting, Kaggle rice paddy competition.

### Tree based methods

- 1R (a single binary split decision tree)

Information that random forest gives you
- out-of-bag error
- How confident are we in our predictions for a particular row of data?
  - variance of predictions from trees in forest.
- What were the most important factors for a prediction on a particular row?
- Which columns are the strongest predictors? Feature importance.
- Which columns are redundant with each other?
- How do predictions vary as we vary feature values?
  - Partial dependence plots

Leo Breiman [Statistical Modeling: The Two Cultures][breiman]

[How to explain gradient boosting][expl-gb], Terence Parr and Jeremy Howard

### Kaggle rice disease recognition

convnext

test-time augmentation

[breiman]: https://www.semanticscholar.org/paper/Statistical-modeling%3A-The-two-cultures-Breiman/e5df6bc6da5653ad98e754b08f63326c2e52b372
[expl-gb]: https://explained.ai/gradient-boosting/
[l6]: https://course.fast.ai/Lessons/lesson6.html


## Lesson 7: collaborative filtering

[Lesson 7][l7] summary: Kaggle rice paddy competition, ensembling, Multi-target models, Collaborative filtering.

[Things that confused me about cross-entropy][said-ce] by Chris Said

matrix factorization

Multiplying by a one-hot encoded vector is equivalent to doing a lookup.

[l7]: https://course.fast.ai/Lessons/lesson7.html
[said-ce]: https://chris-said.io/2020/12/26/two-things-that-confused-me-about-cross-entropy/


## Lesson 8: Convolutions

[Lesson 8][l8] summary: Convolutions, CNNs, max vs. average pooling, dropout.

[CNNs from different viewpoints][cnnv] by Matthew Kleinsmith

[Activation Functions in Neural Networks][actss] by Sagar Sharma

[Dropout: A Simple Way to Prevent Neural Networks from Overfitting][srivastava]


[l8]: https://course.fast.ai/Lessons/lesson8.html
[cnnv]: https://medium.com/impactai/cnns-from-different-viewpoints-fab7f52d159c
[actss]: https://towardsdatascience.com/activation-functions-neural-networks-1cbd9f8d91d6
[srivastava]: https://www.cs.toronto.edu/~rsalakhu/papers/srivastava14a.pdf



## Lesson 9: Ethics for Data Science

What could go wrong?

- Toxic feedback loops.
- No way to identify and address mistakes.
- Bias
- Use of technology for harmful purposes.

Questions to ask:

- Should we be doing this?
- What bias is in the data?
- Can the code and data be audited?
- What are error rates for different subgroups?
- What is the accuracy of a rule-based alternative?
- What is the process to handle appeals or mistakes?
- How diverse is the team that built it?


### Ethics resources

- [A Framework for Understanding Unintended Consequences of Machine Learning][l9-1] by Harini Suresh and John V. Guttag
- [Tutorial: 21 fairness definitions and their politics][l9-2] by Arvind Narayanan
- [Ethics in Technology Practice][l9-3] from SCU Markkula Center for Applied Ethics
- [Datasheets for Datasets][l9-4]


[l9-1]: https://aps.arxiv.org/abs/1901.10002v2
[l9-2]: https://www.youtube.com/watch?v=jIXIuYdnyyk
[l9-3]: https://www.scu.edu/ethics-in-technology-practice/
[l9-4]: https://arxiv.org/abs/1803.09010
