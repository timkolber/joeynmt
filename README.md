# &nbsp; ![Joey-NMT with Deliberation networks](joey2-small.png) Joey NMT
[![build](https://github.com/joeynmt/joeynmt/actions/workflows/main.yml/badge.svg)](https://github.com/joeynmt/joeynmt/actions/workflows/main.yml)
[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)


## Goal and Purpose
:koala: Joey NMT framework is developed for educational purposes.
It aims to be a **clean** and **minimalistic** code base to help novices 
find fast answers to the following questions.
- :grey_question: How to implement classic NMT architectures (RNN and Transformer) in PyTorch?
- :grey_question: What are the building blocks of these architectures and how do they interact?
- :grey_question: How to modify these blocks (e.g. deeper, wider, ...)?
- :grey_question: How to modify the training procedure (e.g. add a regularizer)?

In contrast to other NMT frameworks, we will **not** aim for the most recent features
or speed through engineering or training tricks since this often goes in hand with an
increase in code complexity and a decrease in readability. :eyes:

However, Joey NMT re-implements baselines from major publications.

Check out the detailed [documentation](https://joeynmt.readthedocs.io) and our
[paper](https://arxiv.org/abs/1907.12484).

## Contributors
Joey NMT was initially developed and is maintained by [Jasmijn Bastings](https://github.com/bastings) (University of Amsterdam) and [Julia Kreutzer](https://juliakreutzer.github.io/) (Heidelberg University), now both at Google Research. [Mayumi Ohta](https://www.cl.uni-heidelberg.de/statnlpgroup/members/ohta/) at Heidelberg University is continuing the legacy.

Welcome to our new contributors :hearts:, please don't hesitate to open a PR or an issue
if there's something that needs improvement!

## Features
Joey NMT implements the following features (aka the minimalist toolkit of NMT :wrench:):
- Recurrent Encoder-Decoder with GRUs or LSTMs
- Transformer Encoder-Decoder
- Attention Types: MLP, Dot, Multi-Head, Bilinear
- Word-, BPE- and character-based tokenization
- BLEU, ChrF evaluation
- Beam search with length penalty and greedy decoding
- Customizable initialization
- Attention visualization
- Learning curve plotting
- Scoring hypotheses and references



## Installation
Joey NMT is built on [PyTorch](https://pytorch.org/). Please make sure you have a compatible environment.
We tested Joey NMT 2.0 with
- python 3.10
- torch 1.12.1
- cuda 11.6

> :warning: **Warning**
> When running on **GPU** you need to manually install the suitable PyTorch version 
> for your [CUDA](https://developer.nvidia.com/cuda-zone) version.
> For example, you can install PyTorch 1.12.1 with CUDA v11.6 as follows:
> ```
> $ pip install --upgrade torch==1.12.1 --extra-index-url https://download.pytorch.org/whl/cu116
> ```
> See [PyTorch installation instructions](https://pytorch.org/get-started/locally/).


You can install Joey NMT either A. via [pip](https://pypi.org/project/joeynmt/) or B. from source.

### A. Via pip (the latest stable version)
```bash
$ pip install joeynmt
```


### B. From source (for local development)
1. Clone this repository:
  ```bash
  $ git clone https://github.com/joeynmt/joeynmt.git
  $ cd joeynmt
  ```
2. Install Joey NMT and it's requirements:
  ```bash
  $ pip install -e .
  ```
3. Run the unit tests:
  ```bash
  $ python -m unittest
  ```

I ran my code with the packages described in requirements.txt on python 3.10. The config files for the new models are located in the configs directory.
