** **This is work in progress** **

# BETO: Spanish BERT

BETO is a [BERT model](https://github.com/google-research/bert) trained on a [big Spanish corpus](https://github.com/josecannete/spanish-corpora). BETO is of size similar to a BERT-Base and was trained with the Whole Word Masking technique. Below you find Tensorflow and Pytorch checkpoints for the uncased and cased versions, as well as some results for Spanish benchmarks comparing BETO with [Multilingual BERT](https://github.com/google-research/bert/blob/master/multilingual.md) as well as other (not BERT-based) models.

## Download

| | | | |
|-|:--------:|:-----:|:----:|
|BETO uncased|[tensorflow weights](https://users.dcc.uchile.cl/~jperez/beto/uncased_2M/tensorflow_weights.tar.gz) | [pytorch weights](https://users.dcc.uchile.cl/~jperez/beto/uncased_2M/pytorch_weights.tar.gz) | [vocab](https://users.dcc.uchile.cl/~jperez/beto/uncased_2M/vocab.txt), [config](https://users.dcc.uchile.cl/~jperez/beto/uncased_2M/bert_config.json) |
|BETO cased| [tensorflow weights](https://users.dcc.uchile.cl/~jperez/beto/cased_2M/tensorflow_weights.tar.gz) | [pytorch weights](https://users.dcc.uchile.cl/~jperez/beto/cased_2M/pytorch_weights.tar.gz) | [vocab](https://users.dcc.uchile.cl/~jperez/beto/cased_2M/vocab.txt), [config](https://users.dcc.uchile.cl/~jperez/beto/cased_2M/config.json) |

All models use a vocabulary of about 31k BPE subwords constructed using SentencePiece and were trained for 2M steps. 

## Benchmarks

The following table shows some BETO results in the Spanish version of every task. 
We compare BETO (cased and uncased) with the Best Multilingual BERT results that 
we found in the literature (as of October 2019) highlighting 
the results whenever BETO ourperform Multilingual BERT for the Spanish task. 
The table also shows some alternative methods for the same tasks (not necessarily BERT-based methods).
References for all methods can be found [here](#references).

|Task   | BETO-cased    | BETO-uncased  | Best Multilingual BERT    | Other results                  |
|-------|--------------:|--------------:|--------------------------:|-------------------------------:|
|XNLI   | -----         | **80.15**     | 78.50 [2]                 | 80.80 [5], 77.80 [1], 73.15 [4]|
|POS    | -----         | **98.44**     | 97.10 [2]                 | 98.91 [6], 96.71 [3]           |
|PAWS-X | -----         | 89.55         | 90.70 [8]                 |
|NER-C  | -----         | 81.70         | 87.38 [2]                 | 87.18 [3]                      |
|MLDoc  | 95.27         | 95.25         | 95.70 [2]                 | 88.75 [4]                      |

## Example of use

For further details on how to use BETO you can visit the amazing [🤗Transformers repo](https://github.com/huggingface/transformers), starting by the [Quickstart section](https://huggingface.co/transformers/quickstart.html).


## Acknowledgments

We thank [Adereso](https://www.adere.so/) for kindly providing support for traininig BETO-uncased, and the [Millennium Institute for Foundational Research on Data](https://imfd.cl/en/)
that provided support for training BETO-cased.


## References

* [1] [Original Multilingual BERT](https://github.com/google-research/bert/blob/master/multilingual.md)
* [2] [Multilingual BERT on "Beto, Bentz, Becas: The Surprising Cross-Lingual Effectiveness of BERT"](https://arxiv.org/pdf/1904.09077.pdf)
* [3] [Multilingual BERT on "How Multilingual is Multilingual BERT?"](https://arxiv.org/pdf/1906.01502.pdf)
* [4] [LASER](https://arxiv.org/abs/1812.10464)
* [5] [XLM (MLM+TLM)](https://arxiv.org/pdf/1901.07291.pdf)
* [6] [UDPipe on "75 Languages, 1 Model: Parsing Universal Dependencies Universally"](https://arxiv.org/pdf/1904.02099.pdf)
* [7] [Multilingual BERT on "Sequence Tagging with Contextual and Non-Contextual Subword Representations: A Multilingual Evaluation"](https://arxiv.org/pdf/1906.01569.pdf)
* [8] [Multilingual BERT on "PAWS-X: A Cross-lingual Adversarial Dataset for Paraphrase Identification"](https://arxiv.org/abs/1908.11828)
