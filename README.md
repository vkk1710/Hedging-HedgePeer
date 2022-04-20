# HedgePeer
An Uncertainty Detection Dataset based on Peer Reviews

## Outline

- Motivation 
- Dataset : Download
- Experiments
- Acknowledgement
- Bib

## Motivation

Peer reviews are a form of scientific self-evaluation of research articles that may consist of reviews filled with uncertain information. This may be due to multiple reasons like : less proficient reviewer (in the field of publication), a polite form of writing, etc. 

Why identifying uncertainty in peer reviews important? Peer Reviews often consist the confidence level of the reviewer (manually entered by the reviewer). Many a times, a confident reviewer tends to write lackluster reviews with high degree of uncertainty. Hence, gauging the confidence of the reviewer based on their reviews is appropriate. 

Identifying uncertainty in reviews may be used as a proxy for gauging the actual confidence of the reviewer. This is where HedgePeer helps! It is the largest uncertainty detection dataset based on peer reviews.

## Dataset : Download

We introduce HedgePeer, a new dataset for uncertainty detection based on peer reviews. Download the dataset from the following link:

[HedgePeer.zip](https://drive.google.com/drive/folders/1NEmZAgMtbF8gbAtnOXQj-Dfd5F3SqoJe?usp=sharing)

The dataset is in the format of Jsonlines. Please read the README.txt in the folder for additional details.

## Experiments

We have trained several baselines on the BioScope and HedgePeer datasets. The variants used are :
- Simple Baseline
- Multi-Task Learning Baselines
  - Sentiment Intensity and POS tagging Scaffolds
  - Sentiment Intensity Scaffold and POS Late Fusion

Below are our results for Hedge cue and Span detection of several baselines on the HedgePeer dataset:

### Results on Hedge Cue Detection

| Model | Transformer | F1 Score |
| --- | --- | --- |
| Simple Baseline | SciBERT | 76.9 |
| Simple Baseline | BERT | 79.4 |
| Simple Baseline | XLNet | **84.0** |
| MTL with Sentiment | SciBERT | 72.0 |
| MTL with Sentiment | BERT | 80.6 |
| MTL with Sentiment | XLNet | 82.4 |
| MTL with Sentiment+POS | SciBERT | 72.0 |
| MTL with Sentiment+POS | BERT | 72.0 |
| MTL with Sentiment+POS | XLNet | 74.8 |
| MTL with Sentiment+POS LF | SciBERT | 71.0 |
| MTL with Sentiment+POS LF | BERT | 72.1 |
| MTL with Sentiment+POS LF | XLNet | 74.5 |

### Results on Hedge Span Detection

| Model | Transformer | F1 Score |
| --- | --- | --- |
| Simple Baseline | SciBERT | 96.6 |
| Simple Baseline | BERT | 97.0 |
| Simple Baseline | XLNet | **97.3** |
| MTL with Sentiment | SciBERT | 96.3 |
| MTL with Sentiment | BERT | 97.2 |
| MTL with Sentiment | XLNet | 97.2 |
| MTL with Sentiment+POS | SciBERT | 96.9 |
| MTL with Sentiment+POS | BERT | 97.0 |
| MTL with Sentiment+POS | XLNet | **97.3** |
| MTL with Sentiment+POS LF | SciBERT | 96.7 |
| MTL with Sentiment+POS LF | BERT | 97.0 |
| MTL with Sentiment+POS LF | XLNet | 97.1 |

## Acknowledgement

## Bib
