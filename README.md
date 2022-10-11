# iEnhancer-ELM
📋 iEnhancer-ELM: Learning Explainable Contextual Information to Improve Enhancer Identification using Enhancer Language Models

## Abstract

Enhancers are important **cis**-regulatory elements that regulate a wide range of biological functions and enhance the transcription of target genes. In order to efficiently identify enhancers, many state-of-the-art computational methods have been proposed. One of challenges for computational methods is learning effective long-distance contextual features. Recently, several works took the biological sequences as natural sentences and employed the language model techniques from natural language processing to capture the long-distance contextual information. In this paper, we propose an enhancer language model **(iEnhancer-ELM)** for enhancer identification by incorporating a pre-trained BERT-based DNA model. iEnhancer-ELM treats enhancer sequences as natural sentences that are composed of k-mer nucleic acids to extract informative biological features from raw enhancer sequences. Benefiting from the complementary information in various k-mer (k=3,4,5,6) tokens, we ensemble four iEnhancer-ELM models for improving enhancer identification. The experimental results show that our model achieve an accuracy of **83.00%**, outperforming competing state-of-the-art methods. Moreover, **40%** of motifs found by iEnhancer-ELM can exhibit statistical and biological significance, demonstrating our model is explainable and has a potential ability to reveal the biological mechanism. 

## 



## Benchmark Dataset
The benchmark dataset used in our article is from [Liu et al.](https://academic.oup.com/bioinformatics/article-abstract/34/22/3835/5034432), which consists of a training dataset and an independent dataset. In the training dataset, there are 1484 enhancer sequences and 1484 non-enhancer sequences. And there are 742 enhancer sequences and 742 non-enhancer sequences in the independent dataset. The files with a k-mer in its  file name represents the result of our overlapping tokenization result of the training dataset or the independent dataset.

## Code
We add the analysis codes to this folder. In the motif analysis, we refer to codes from [Ji et al.](https://academic.oup.com/bioinformatics/article-abstract/37/15/2112/6128680). We add the result of motif analysis in the folder of 'atten'. The folder of 'analysis' contains the t-SNE analysis process of sequence embedding.

In addition, the pre-trianed BERT-based DNA model is from [Ji et al.](https://academic.oup.com/bioinformatics/article-abstract/37/15/2112/6128680). In practice, we attach a 2-layer perceptron network as the classifier followed the pre-trained model and then fine-tune these pre-trianed weights on our enhancer benchmark dataset. We can download the pre-trained models and their corresponding iEnhancer-ELM models in this [link_of_models](https://drive.google.com/drive/folders/10Gr9RzB_tZGosA-aSwWHB3pB68AvNk5_?usp=sharing). 
