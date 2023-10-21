# BETO: Spanish BERT

BETO es un [modelo BERT](https://github.com/google-research/bert) entrenado sobre un gran [corpus en Español](https://github.com/josecannete/spanish-corpora). BETO es de tamaño similar a Bert-Base y fue entrenado con la técnica Whole Word Masking. A continuación, encontrarás checkpoints para Tensorflow y Pytorch de las versiones uncased y cased, así como algunos resultados de pruebas comparativas en Español que comparan BETO con [Multilingual BERT](https://github.com/google-research/bert/blob/master/multilingual.md), así como otros modelos (no BERT-Based).

## Download

|              |                  HuggingFace Model Repository                  |
|:------------:|:--------------------------------------------------------------:|
| BETO uncased | [dccuchile/bert-base-spanish-wwm-uncased](https://huggingface.co/dccuchile/bert-base-spanish-wwm-uncased) |
|  BETO cased  |  [dccuchile/bert-base-spanish-wwm-cased](https://huggingface.co/dccuchile/bert-base-spanish-wwm-cased)  |

Todos los modelos utilizan un vocabulario de aproximadamente 31.000 subpalabras BPE construidas con SentencePiece y fueron entrenados para 2 millones de steps.

## Benchmarks

La siguiente tabla muestra algunos resultados BETO en la versión en español de cada tarea.
Comparamos BETO (cased y uncased) con los mejores resultados de Multilingual BERT que
encontramos en la literatura (a octubre del 2019).
La tabla también muestra algunos métodos alternativos para las mismas tareas (no necesariamente BERT-based).
Las referencias de todos los métodos se pueden encontrar [aquí](#references).

|Task   | BETO-cased    | BETO-uncased  | Best Multilingual BERT    | Other results                  |
|-------|--------------:|--------------:|--------------------------:|-------------------------------:|
|[POS](https://lindat.mff.cuni.cz/repository/xmlui/handle/11234/1-1827)    | **98.97**     | 98.44     | 97.10 [2]                 | 98.91 [6], 96.71 [3]           |
|[NER-C](https://www.kaggle.com/nltkdata/conll-corpora)  | [**88.43**](https://github.com/gchaperon/beto-benchmarks/blob/master/conll2002/dev_results_beto-cased_conll2002.txt)         | 82.67         | 87.38 [2]                 | 87.18 [3]                      |
|[MLDoc](https://github.com/facebookresearch/MLDoc)  | [95.60](https://github.com/gchaperon/beto-benchmarks/blob/master/MLDoc/dev_results_beto-cased_mldoc.txt)        | [**96.12**](https://github.com/gchaperon/beto-benchmarks/blob/master/MLDoc/dev_results_beto-uncased_mldoc.txt)     | 95.70 [2]                 | 88.75 [4]                      |
|[PAWS-X](https://github.com/google-research-datasets/paws/tree/master/pawsx) | 89.05         | 89.55         | 90.70 [8]                 |
|[XNLI](https://github.com/facebookresearch/XNLI)   | **82.01**         | 80.15     | 78.50 [2]                 | 80.80 [5], 77.80 [1], 73.15 [4]|

## Example of use

Para obtener más detalles sobre cómo usar BETO, puede visitar la biblioteca [🤗Huggingface Transformers](https://github.com/huggingface/transformers), comenzando por la [Quickstart section](https://huggingface.co/docs/transformers/tasks/sequence_classification). Se puede acceder a los modelos BETO simplemente como [`'dccuchile/bert-base-spanish-wwm-cased'`](https://huggingface.co/dccuchile/bert-base-spanish-wwm-cased) y [`'dccuchile/bert-base-spanish-wwm-uncased'`](https://huggingface.co/dccuchile/bert-base-spanish-wwm-uncased) utilizando la biblioteca Transformers. Un ejemplo de como usar los modelos en esta página se puede encontrar, en este [colab notebook](https://colab.research.google.com/drive/1pYOYsCU59GBOwztkWCw5PTsqBiJbRy4S?usp=sharing).


## Acknowledgments

Agradecemos a [Adereso](https://www.adere.so/) por brindar amablemente apoyo para entrenar BETO-uncased, y el [Millennium Institute for Foundational Research on Data](https://imfd.cl/en/) que brindó apoyo para el entrenamiento de BETO-cased. También gracias a Google por ayudarnos con el programa [TensorFlow Research Cloud](https://www.tensorflow.org/tfrc). 

## Citation

[Spanish Pre-Trained BERT Model and Evaluation Data](https://arxiv.org/abs/2308.02976)

Para citar este recurso en una publicación por favor use lo siguiente:

```
@inproceedings{CaneteCFP2020,
  title={Spanish Pre-Trained BERT Model and Evaluation Data},
  author={Cañete, José and Chaperon, Gabriel and Fuentes, Rodrigo and Ho, Jou-Hui and Kang, Hojin and Pérez, Jorge},
  booktitle={PML4DC at ICLR 2020},
  year={2020}
}
```


## License Disclaimer
La licencia CC BY 4.0 describe mejor nuestras intenciones para nuestro trabajo. Sin embargo, no estamos seguros de que todos los conjuntos de datos utilizados para entrenar BETO tengan licencias compatibles con CC BY 4.0 (especialmente para uso comercial). Por favor, use a su propia discreción y verifique que las licencias de los recursos de texto originales coincidan con sus necesidades.


## References

* [1] [Original Multilingual BERT](https://github.com/google-research/bert/blob/master/multilingual.md)
* [2] [Multilingual BERT on "Beto, Bentz, Becas: The Surprising Cross-Lingual Effectiveness of BERT"](https://arxiv.org/pdf/1904.09077.pdf)
* [3] [Multilingual BERT on "How Multilingual is Multilingual BERT?"](https://arxiv.org/pdf/1906.01502.pdf)
* [4] [LASER](https://arxiv.org/abs/1812.10464)
* [5] [XLM (MLM+TLM)](https://arxiv.org/pdf/1901.07291.pdf)
* [6] [UDPipe on "75 Languages, 1 Model: Parsing Universal Dependencies Universally"](https://arxiv.org/pdf/1904.02099.pdf)
* [7] [Multilingual BERT on "Sequence Tagging with Contextual and Non-Contextual Subword Representations: A Multilingual Evaluation"](https://arxiv.org/pdf/1906.01569.pdf)
* [8] [Multilingual BERT on "PAWS-X: A Cross-lingual Adversarial Dataset for Paraphrase Identification"](https://arxiv.org/abs/1908.11828)
