# README
Implementation of OpenAI paper ["An Empirical Model of Large-Batch Training"](https://arxiv.org/pdf/1812.06162.pdf) for Fastai V2. 

The code is based on the batch size finder implementation for Fastai V1 by DanyWind ([repo V1](https://github.com/DanyWind/fastai_bs_finder) / [blog](https://towardsdatascience.com/implementing-a-batch-size-finder-in-fastai-how-to-get-a-4x-speedup-with-better-generalization-813d686f6bdf) / [discussion](https://forums.fast.ai/t/batch-size-finder-from-openai-implemented-using-fastai/57620)). 

This implementation differs on:
1. It implements exactly the original article and not an aproximation (by default). 
1. Fixes a couple of bugs in noise and scale values. However, they didn't affect on Simple Noise Scale value.

However, you could use the DanyWind aproximation by settting simulate_multi_gpus to False. DanyWind aproximation is faster but numerically more inestable and finds a Simple Noise Scale smaller than the original Simple Noise Scale.