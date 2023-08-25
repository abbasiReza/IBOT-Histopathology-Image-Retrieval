# Histopathology Image Retrieval- IBOT 
![Histopathology Image Retrieval](https://github.com/bytedance/ibot/blob/main/.github/framework.png)
## Description

This project implements an image retrieval system for histopathology images using the iBoT (Image BERT Pre-Training with Online Tokenizer) self-supervised learning model. The goal is to retrieve similar histopathology images given a query image.

## Model 

The iBoT model is used for encoding images into feature vectors that can be compared for similarity. iBoT is pre-trained on a large dataset of unlabeled images to learn useful visual representations. These visual features are then used to index and retrieve similar images.

## Datasets

The model is trained and evaluated on the following histopathology image datasets:

- [BracS](https://www.bracs.icar.cnr.it/) - Breast Cancer Histopathology Image Dataset
- [CRC](https://warwick.ac.uk/fac/cross_fac/tia/data/extended_crc_grading/) - Colorectal Cancer Histopathology Images
- [BATCH](https://iciar2018-challenge.grand-challenge.org/Dataset/) - BreAst Cancer Histology Challenge Dataset  

## Usage

The image retrieval system provides an interface to upload a query histology image. It then indexes through the dataset encodings to find the most similar images based on the iBoT features. The top k retrieved images are returned, ranked by similarity. 

The project provides code to train the iBoT encoder as well as utilities to index and search the image datasets.

## References

[iBoT Paper](https://arxiv.org/abs/2101.12091)
