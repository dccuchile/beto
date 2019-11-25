# BETO is Spanish BERT

In this repo we open-source our SpanishBERT model which is a BERT-Base WWM (Whole Word Mask) model trained on Spanish Corpora.

# Download

### Tensorflow

Uncased BETO ([vocab](https://users.dcc.uchile.cl/~jperez/beto/vocab.txt), [config](https://users.dcc.uchile.cl/~jperez/beto/bert_config.json), [weights](https://users.dcc.uchile.cl/~jperez/beto/tensorflow_weights.tar.gz))

Cased BETO ([vocab](www.google.com), [config](www.google.com), [weights](www.google.com)) - Coming soon!

### PyTorch

Uncased BETO ([vocab](https://users.dcc.uchile.cl/~jperez/beto/vocab.txt), [config](https://users.dcc.uchile.cl/~jperez/beto/bert_config.json), [weights](https://users.dcc.uchile.cl/~jperez/beto/pytorch_weights.tar.gz))

Cased BETO ([vocab](www.google.com), [config](www.google.com), [weights](www.google.com)) - Coming soon!

# Example of use

For further details you can visit the amazing [🤗 Transformers](https://github.com/huggingface/transformers) repo, starting by the [Quickstart section](https://huggingface.co/transformers/quickstart.html).

# Evaluation

This is WIP: For now you can visit [beto-benchmarking](https://github.com/josecannete/beto-benchmarking) to see the progress.

# Training details

### Corpora

We used the Spanish Unnanotated Corpora to train. For further details please visit the respective repo: [SUC](https://github.com/josecannete/spanish-corpora)

### Vocabulary

We used a vocabulary of about 31k BPE subwords. We used SentencePiece to construct it.

# Acknowledgments

Thanks to [Adereso](www.adere.so) for provide efforts and Cloud TPUs to train BETO. 

# FAQ

# References
#### BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding ([paper](https://arxiv.org/abs/1810.04805), [code](https://github.com/google-research/bert))

#### 🤗 Transformers: State-of-the-art Natural Language Processing for TensorFlow 2.0 and PyTorch ([paper](https://arxiv.org/abs/1910.03771), [code](https://github.com/huggingface/transformers))
