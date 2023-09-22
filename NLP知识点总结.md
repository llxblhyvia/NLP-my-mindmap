NLP知识点总结

[toc]

# NLP基础知识

## Information Retrieval

### LSH算法



## Tokenization

https://huggingface.co/learn/nlp-course/chapter2/4?fw=pt完美

##### unicode与UTF-8

前置基础知识

https://blog.csdn.net/zhusongziye/article/details/84261211?spm=1001.2101.3001.6650.2&utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-2-84261211-blog-129034732.235%5Ev38%5Epc_relevant_anti_t3&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-2-84261211-blog-129034732.235%5Ev38%5Epc_relevant_anti_t3&utm_relevant_index=5

### Word level

会引入过多的<unknown>

### character level

Tokens 过多

### Subword 

close to no unknown tokens

### BPE（subword tokenization）

https://zhuanlan.zhihu.com/p/424631681

#### BBPE (byte-level BPE)

used in GPT-2

https://zhuanlan.zhihu.com/p/146114164

#### WordPiece

used in BERT ？？

#### SentencePiece or Unigram

as used in several **multilingual** models





# RNN model

## ELMo

cs224n

## 

# LLM

## Transformer 

Encoder model: auto-encoding model 

Decoder model: auto-regressive model

Encoder-decoder model: seq2seq model



## 1.Encoder model: auto-encoding model 

### 1.1 BERT

#### Uncased v.s. Cased

Uncased 表示在 wordPiece tokenization 之前文本已经变成小写了，例如，John

Smith becomes john smnith。 Uncased 模型也去掉了所有重音标志。

Cased 表示保留了真实的大小写和重音标记。

**通常**，除非你已经知道大小写信息对你的任务来说很重要 （例如，命名实体识别或词性标记），否则 **Uncased模型会更好**。

### 1.2 RoBERTa

https://zhuanlan.zhihu.com/p/347861417

### 1.3 DeBERTa

#### v1 

https://zhuanlan.zhihu.com/p/505615608

> 文章提出了两种改进BERT预训练的方法：第一种是注意解耦机制，该机制将一个单词的表征由单词的内容和位置编码组成，并使用解耦矩阵计算单词之间在内容和相对位置上的注意力权重；第二种是引入一个增强的掩码解码器(EMD)，它取代原有输出的Softmax来预测用于MLM预训练的被mask掉的token。使用这两种技术，新的预训练语言模型DeBERTa在许多下游NLP任务上的表现都优于RoBERTa和BERT。DeBERTa这项工作展示了探索自注意的词表征解耦以及使用任务特定解码器改进预训练语言模型的潜力。

#### v3

看原文

## 2.Decoder model: auto-regressive model

### 2.1 GPT

#### 2.1.1 GPT 1/2/3

##### RMS normalization

##### Rotary Embedding

##### SwiGLU

#### 2.1.2 instructGPT(3.5)

SFT+RM+RL->RLHF

#### 2.1.3 GPT4



## 3.Encoder-decoder model: seq2seq model

### 3.1 T5

 [T5](https://huggingface.co/t5-base) is pretrained by replacing random spans of text (that can contain several words) with a single mask special word, and the objective is then to predict the text that this mask word replaces.

### 3.2 BART

### 





## PaLM todo

## Llama todo

### 1

### 2

## T5

## GLM

## LoRA









