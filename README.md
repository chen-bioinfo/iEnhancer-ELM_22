# iEnhancer-ELM
iEnhancer-ELM: Learning Explainable Contextual Information to Improve Enhancer Identification using Enhancer Language Models

## Benchmark Dataset
The benchmark dataset used in our article is from [Liu et al.](https://academic.oup.com/bioinformatics/article-abstract/34/22/3835/5034432), which consists of a training dataset and an independent dataset. In the training dataset, there are 1484 enhancer sequences and 1484 non-enhancer sequences. And there are 742 enhancer sequences and 742 non-enhancer sequences in the independent dataset. The files with a k-mer in its  file name represents the result of our overlapping tokenization result of the training dataset or the independent dataset.

## Code
We add the analysis codes to this folder. In the motif analysis, we refer to codes from Ji et al.[2]. We add the result of motif analysis in the folder of 'atten'. The folder of 'analysis' contains the t-SNE analysis process of sequence embedding.

In addition, the pre-trianed BERT-based DNA model is from [Ji et al.](https://academic.oup.com/bioinformatics/article-abstract/37/15/2112/6128680). In practice, we attach a 2-layer perceptron network as the classifier followed the pre-trained model and then fine-tune these pre-trianed weights on our enhancer benchmark dataset. We can download the pre-trained models and their corresponding iEnhancer-ELM models in this [link for models](https://drive.google.com/drive/folders/10Gr9RzB_tZGosA-aSwWHB3pB68AvNk5_?usp=sharing). 
