---
layout:   post
title:    "[ZK Lab] #2: Platform - Hugging Face"
subtitle: "BLOG + LINK"
category: studylog
tags: zklab
---

# [ZK Lab] #2: Platform - Hugging Face

## [Hugging Face](https://huggingface.co/)

### Goal
Hugging Face Hub is building the largest collection of models, datasets and metrics in order to democratize and advance AI for everyone.

### Repository
The Hugging Face Hub hosts Git-based repositories which are storage spaces that can contain all your files.

The Hub currently hosts three different repo types:
- models
- datasets
- Spaces, which are ML demo apps

These repositories have multiple advantages over other hosting solutions:
- versioning
- commit history and diffs
- branches

On top of that, Hugging Face Hub repositories have many other advantages, for instance for models:
- Model repos provide useful metadata about their tasks, languages, metrics, etc.
- Anyone can play with the model directly in the browser!
- Training metrics charts are displayed if the repository contains TensorBoard traces.
- An API is provided to use the models in production settings.
- [Over 10 frameworks](https://huggingface.co/docs/hub/libraries) such as Transformers, Asteroid and ESPnet support using models from the Hugging Face Hub.

### widget
Many model repos have a widget that allows anyone to do inference directly in the browser.

Some examples:

- [Named Entity Recognition](https://huggingface.co/spacy/en_core_web_sm?text=My+name+is+Sarah+and+I+live+in+London) using spaCy[https://spacy.io/].
- [Image Classification](https://huggingface.co/google/vit-base-patch16-224) using [Transformers](https://github.com/huggingface/transformers).
- [Text to Speech](https://huggingface.co/julien-c/ljspeech_tts_train_tacotron2_raw_phn_tacotron_g2p_en_no_space_train) using [ESPnet](https://github.com/espnet/espnet).
- [Sentence Similarity](https://huggingface.co/osanseviero/full-sentence-distillroberta3) using [Sentence Transformers](https://github.com/UKPLab/sentence-transformers).

You can try out all the widgets [here](https://huggingface-widgets.netlify.app/).

### Inference API
The Inference API allows you to send HTTP requests to models in the Hugging Face Hub. The Inference API is 2x to 10x faster than the widgets.

### Explore Hugging Face Hub

<iframe width="735" height="414" src="https://www.youtube.com/embed/XvSGPZFEjDY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Model's Type of Inference API and Widget
- `pipeline_tag`: determine which pipeline and widget to display
- `config.json`: transformers

### Load/Push from/to the Hub

<iframe width="735" height="414" src="https://www.youtube.com/embed/rkCly_cbMBk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
