---
layout:   post
title:    "Attention Mechanism"
subtitle: "BLOG + LINK"
category: studylog
tags: dl
---

# Attention Mechanism



## Encoder-Decoder in NLP

Encoder-Decoder This framework is a good illustration of the core ideas of machine learning:

> Transforming real-world problems into mathematical problems and solving real-world problems by solving mathematical problems.

- Encoder's role is to "transform real problems into mathematical problems."

- Decoder's role is to "solve mathematical problems and transform them into real-world solutions."

### Notes
- Regardless of the length of the input and output, the length of the vector in the middle (the output of encoder) is fixed (this is also its drawback, as explained below).
-  Different encoders and decoders can be selected depending on the task (can be one RNN But usually its variant LSTM Or CRANE).

As long as it conforms to the above framework, it can be collectively referred to as the Encoder-Decoder model. Speaking of the Encoder-Decoder model, a term is often mentioned - Seq2Seq.

### Seq2Seq

Seq2Seq (short for Sequence-to-sequence), as literally, enters a sequence and outputs another sequence. The most important aspect of this structure is that the length of the input sequence and the output sequence are variable. 

### Origin of Seq2Seq

Before the Seq2Seq framework was proposed, deep neural networks achieved very good results in image classification and other issues. In the problem that it is good at solving, the input and output can usually be represented as a fixed-length vector. If the length is slightly changed, the zero-padding operation is used.

However, many important issues, such as machine translation, speech recognition, automatic dialogue, etc., are expressed in sequence, and their length is not known in advance. Therefore, how to break through the limitations of the previous deep neural network, so that it can adapt to these scenarios, has become a research hotspot since 2013, and the Seq2Seq framework came into being.

### Relationship between "Seq2Seq" and "Encoder-Decoder"

Seq2Seq does not specifically refer to specific methods. For the purpose of "input is a sequence, output is also a sequence", it can be collectively referred to as Seq2Seq model.

The specific methods used by Seq2Seq are basically in the scope of the Encoder-Decoder model.

To sum up:

- Seq2Seq belongs to the broad category of Encoder-Decoder
- Seq2Seq emphasizes the purpose, Encoder-Decoder emphasizes the method


### Defects of Encoder-Decoder

When the input information is too long, some information will be lost in the output.

Attention solves the problem of information loss.


## Principle of Attention

Attention is a technique that mimics cognitive attention. The effect enhances some parts of the input data while diminishing other parts — the thought being that the network should devote more focus to that small but important part of the data. Learning which part of the data is more important than others depends on the context and is trained by gradient descent.

In a nutshell, attention in deep learning can be broadly interpreted as a vector of importance weights: in order to predict or infer one element, such as a pixel in an image or a word in a sentence, we estimate using the attention vector how strongly it is correlated with (or “attends to” as you may have read in many papers) other elements and take the sum of their values weighted by the attention vector as the approximation of the target.



## Definition of Attention Mechanism in Neural Machine Translation

Say, we have a source sequence $$\mathbf{x}$$ of length $$n$$ and try to output a target sequence $$y$$ of length $$m$$:

$$
\begin{align}
    \mathbf{x} & = [x_1, x_2, ..., x_n]\\
    \mathbf{y} & = [y_1, y_2, ..., y_m]
\end{align}
$$

The encoder is a bidirectional RNN (or other recurrent network setting of your choice) with a forward hidden state $$\overrightarrow{\mathbf{h}_i}$$ and a backward one $$\overleftarrow{\mathbf{h}_i}$$. A simple concatenation of two represents the encoder state. The motivation is to include both the preceding and following words in the annotation of one word.

$$
\mathbf{h}_i = [\overrightarrow{\mathbf{h}_i}^\top; \overleftarrow{\mathbf{h}_i}^\top]^\top, \ i = 1,...,n
$$

The decoder network has hidden state $$\mathbf{s}_t = f(\mathbf{s}_{t-1}, y_{t-1}, \mathbf{c}_t)$$ for the output word at position $$t$$, $$t = 1, ..., m$$, where the context vector $$\mathbf{c}_t$$ is a sum of hidden states of the input sequence, weighted by alignment scores:

$$
\begin{align}
    \mathbf{c}_t & = \sum_{i=1}^n \alpha_{t,i} \mathbf{h_i} \\
    \alpha_{t,i} & = \text{align}(y_t, x_i) \\
    & = \frac{\exp(\text{score}(\mathbf{s}_{t-1}, \mathbf{h}_i))}{\sum_{i' = 1}^n \exp(\text{score}(\mathbf{s}_{t-1}, \mathbf{h}_{i'}))}
\end{align}
$$

The alignment model assigns a score $$\alpha_{t, i}$$ to the pair of input at position $$i$$ and output at position $$t$$, $$(y_t, x_i)$$,  based on how well they match. The set of $$\{\alpha_{t, i\}$$ are weights defining how much of each source hidden state should be considered for each output. In Bahdanau’s paper, the alignment score $$\alpha$$ is parametrized by a **feed-forward network** with a single hidden layer and this network is jointly trained with other parts of the model. The score function is therefore in the following form, given that tanh is used as the non-linear activation function:

$$
\text{score}(\mathbf{s}_t, \mathbf{h}_i) = \mathbf{v}_a^\top \tanh \left( \mathbf{W}_a \left[ \mathbf{s}_t; \mathbf{h}_i \right] \right)
$$
where both $$\mathbf{v}_a$$ and $$\mathbf{W}_a$$ are weight matrices to be learned in the alignment model.


## Self-Attention
Self-attention, also known as intra-attention, is an attention mechanism relating different positions of a single sequence in order to compute a representation of the same sequence. It has been shown to be very useful in machine reading, abstractive summarization, or image description generation.

The long short-term memory network paper used self-attention to do machine reading. In the example below, the self-attention mechanism enables us to learn the correlation between the current words and the previous part of the sentence.

## Soft vs Hard Attention
In the [show, attend and tell](http://proceedings.mlr.press/v37/xuc15.pdf) paper, attention mechanism is applied to images to generate captions. The image is first encoded by a CNN to extract features. Then a LSTM decoder consumes the convolution features to produce descriptive words one by one, where the weights are learned through attention. The visualization of the attention weights clearly demonstrates which regions of the image the model is paying attention to so as to output a certain word.

This paper first proposed the distinction between “soft” vs “hard” attention, based on whether the attention has access to the entire image or only a patch:

- Soft Attention: the alignment weights are learned and placed “softly” over all patches in the source image; essentially the same type of attention as in [Bahdanau et al., 2015](https://arxiv.org/abs/1409.0473).
    - Pro: the model is smooth and differentiable.
    - Con: expensive when the source input is large.
- Hard Attention: only selects one patch of the image to attend to at a time.
    - Pro: less calculation at the inference time.
    - Con: the model is non-differentiable and requires more complicated techniques such as variance reduction or reinforcement learning to train. ([Luong, et al., 2015](https://arxiv.org/abs/1508.04025))





## Advantage of Attention mechanism

3 main reasons:

- Less source

In comparison, the complexity is smaller and the parameters are less than CNN and RNN based model. Therefore, the requirements for computing power are even smaller.

- High speed

Attention solves the problem that RNN cannot be computed in parallel. Each step of the Attention mechanism calculation does not depend on the calculation results of the previous step, so it can be processed in parallel as CNN.


- Good result

Before the introduction of the Attention mechanism, there was a problem that everyone had been annoyed: long-distance information would be weakened, just like people with weak memory, and the same thing could not be remembered in the past.

However, Attention can make model focus without losing important information.



## Reference
[1] Lil'Log: Attention? Attention! ([Link](https://lilianweng.github.io/posts/2018-06-24-attention/#definition))

[2] Zhihu BLOG ([Link](https://zhuanlan.zhihu.com/p/91839581))




