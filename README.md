# BETO: Spanish BERT

BETO is a [BERT model](https://github.com/google-research/bert) trained on a [big Spanish corpus](https://github.com/josecannete/spanish-corpora). BETO is of size similar to a BERT-Base and was trained with the Whole Word Masking technique. Below you find Tensorflow and Pytorch checkpoints for the uncased and cased versions, as well as some results for Spanish benchmarks comparing BETO with [Multilingual BERT](https://github.com/google-research/bert/blob/master/multilingual.md) as well as other (not BERT-based) models.

## Download

|              |                  HuggingFace Model Repository                  |
|:------------:|:--------------------------------------------------------------:|
| BETO uncased | [dccuchile/bert-base-spanish-wwm-uncased](https://huggingface.co/dccuchile/bert-base-spanish-wwm-uncased) |
|  BETO cased  |  [dccuchile/bert-base-spanish-wwm-cased](https://huggingface.co/dccuchile/bert-base-spanish-wwm-cased)  |

All models use a vocabulary of about 31k BPE subwords constructed using SentencePiece and were trained for 2M steps. 

## Benchmarks

The following table shows some BETO results in the Spanish version of every task. 
We compare BETO (cased and uncased) with the Best Multilingual BERT results that 
we found in the literature (as of October 2019). 
The table also shows some alternative methods for the same tasks (not necessarily BERT-based methods).
References for all methods can be found [here](#references).

|Task   | BETO-cased    | BETO-uncased  | Best Multilingual BERT    | Other results                  |
|-------|--------------:|--------------:|--------------------------:|-------------------------------:|
|[POS](https://lindat.mff.cuni.cz/repository/xmlui/handle/11234/1-1827)    | **98.97**     | 98.44     | 97.10 [2]                 | 98.91 [6], 96.71 [3]           |
|[NER-C](https://www.kaggle.com/nltkdata/conll-corpora)  | [**88.43**](https://github.com/gchaperon/beto-benchmarks/blob/master/conll2002/dev_results_beto-cased_conll2002.txt)         | 82.67         | 87.38 [2]                 | 87.18 [3]                      |
|[MLDoc](https://github.com/facebookresearch/MLDoc)  | [95.60](https://github.com/gchaperon/beto-benchmarks/blob/master/MLDoc/dev_results_beto-cased_mldoc.txt)        | [**96.12**](https://github.com/gchaperon/beto-benchmarks/blob/master/MLDoc/dev_results_beto-uncased_mldoc.txt)     | 95.70 [2]                 | 88.75 [4]                      |
|[PAWS-X](https://github.com/google-research-datasets/paws/tree/master/pawsx) | 89.05         | 89.55         | 90.70 [8]                 |
|[XNLI](https://github.com/facebookresearch/XNLI)   | **82.01**         | 80.15     | 78.50 [2]                 | 80.80 [5], 77.80 [1], 73.15 [4]|

## Example of use

For further details on how to use BETO you can visit the [🤗Huggingface Transformers library](https://github.com/huggingface/transformers), starting by the [Quickstart section](https://huggingface.co/docs/transformers/tasks/sequence_classification). 
BETO models can be accessed simply as [`'dccuchile/bert-base-spanish-wwm-cased'`](https://huggingface.co/dccuchile/bert-base-spanish-wwm-cased) and [`'dccuchile/bert-base-spanish-wwm-uncased'`](https://huggingface.co/dccuchile/bert-base-spanish-wwm-uncased) by using the Transformers library. 
An example on how to use the models in this page can be found in [this colab notebook](https://colab.research.google.com/drive/1pYOYsCU59GBOwztkWCw5PTsqBiJbRy4S?usp=sharing).


## Acknowledgments

We thank [Adereso](https://www.adere.so/) for kindly providing support for traininig BETO-uncased, and the [Millennium Institute for Foundational Research on Data](https://imfd.cl/en/)
that provided support for training BETO-cased. Also thanks to Google for helping us with the [TensorFlow Research Cloud](https://www.tensorflow.org/tfrc) program.

## Citation

[Spanish Pre-Trained BERT Model and Evaluation Data](https://arxiv.org/abs/2308.02976)

To cite this resource in a publication please use the following:

```
@inproceedings{CaneteCFP2020,
  title={Spanish Pre-Trained BERT Model and Evaluation Data},
  author={Cañete, José and Chaperon, Gabriel and Fuentes, Rodrigo and Ho, Jou-Hui and Kang, Hojin and Pérez, Jorge},
  booktitle={PML4DC at ICLR 2020},
  year={2020}
}
```


## License Disclaimer
The license CC BY 4.0 best describes our intentions for our work. However we are not sure that all the datasets used to train BETO have licenses compatible with CC BY 4.0 (specially for commercial use). Please use at your own discretion and verify that the licenses of the original text resources match your needs.


## References

* [1] [Original Multilingual BERT](https://github.com/google-research/bert/blob/master/multilingual.md)
* [2] [Multilingual BERT on "Beto, Bentz, Becas: The Surprising Cross-Lingual Effectiveness of BERT"](https://arxiv.org/pdf/1904.09077.pdf)
* [3] [Multilingual BERT on "How Multilingual is Multilingual BERT?"](https://arxiv.org/pdf/1906.01502.pdf)
* [4] [LASER](https://arxiv.org/abs/1812.10464)
* [5] [XLM (MLM+TLM)](https://arxiv.org/pdf/1901.07291.pdf)
* [6] [UDPipe on "75 Languages, 1 Model: Parsing Universal Dependencies Universally"](https://arxiv.org/pdf/1904.02099.pdf)
* [7] [Multilingual BERT on "Sequence Tagging with Contextual and Non-Contextual Subword Representations: A Multilingual Evaluation"](https://arxiv.org/pdf/1906.01569.pdf)
* [8] [Multilingual BERT on "PAWS-X: A Cross-lingual Adversarial Dataset for Paraphrase Identification"](https://arxiv.org/abs/1908.11828)
