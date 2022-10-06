# Notes from FastAI Class 2022

## Lesson 1: Getting started

[Lesson 1][l1] summary: FastAI Library. Bird or not bird image classifier.

Library for setting up a Ubuntu machine: [fastsetup][4]

[fastai: A Layered API for Deep Learning][5] by Jeremy Howard, Sylvain Gugger

[Tanishq Abraham's tutorial on Gradio + HuggingFace Spaces][6]

Assignment: [NZ bird classifier](./notebooks/fastai-homework-1.ipynb).

[l1]: https://course.fast.ai/Lessons/lesson1.html
[l1-4]: https://github.com/fastai/fastsetup
[l1-5]: https://arxiv.org/abs/2002.04688
[l1-6]: https://tmabraham.github.io/blog/gradio_hf_spaces_tutorial


## Lesson 2: Deployment

[Lesson 2][] summary: deployment to Hugging Face Space with Gradio.

- [Gradio tutorial][gradio-tut] from @ilovescience
- [HF Spaces][hfs]
- Installing a python environment:
  - [fastsetup](https://github.com/fastai/fastsetup)
  - Windows: [WSL][WSL] and [Terminal][term]
- tinypets [github](https://github.com/fastai/tinypets) / [site](https://fastai.github.io/tinypets/)
- tinypets fork [github](https://github.com/jph00/tinypets) / [site](https://jph00.github.io/tinypets/)

Assignment: [Deploy NZ bird classifier to Hugging Face](https://huggingface.co/spaces/christopherbare/nz-bird-classifier).

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

### Side notes

- [Python for Data Analysis][p4da], 3ed. Wes McKinney

[nlpnb]: https://www.kaggle.com/code/jhoward/getting-started-with-nlp-for-absolute-beginners
[hftransf]: https://huggingface.co/docs/transformers/index
[viscnn]: https://arxiv.org/abs/1311.2901
[p4da]: https://wesmckinney.com/book/
[l4]: https://course.fast.ai/Lessons/lesson4.html
[metrics]: https://www.fast.ai/posts/2019-09-24-metrics.html
[bots]: https://medium.com/hackernoon/more-than-a-million-pro-repeal-net-neutrality-comments-were-likely-faked-e9f0e3ed36a6
