# Corpus Bootstrapping with LM Perplexity

## Purpose

use language model perplexity to augment a small domain-specific sentence by selecting 'similar' sentences from an unlabeled corpus (e.g. web-crawled data) using 

based on Ramaswamy, Printz, Gopalakrishnan: *A Bootstrap Technique for Building Domain-Dependent Language Models*, available here: http://mirlab.org/conference_papers/International_Conference/ICSLP%201998/PDF/SCAN/SL980611.PDF

## Requirements

- `nltk`
- `kenlm` (LM in C++, install python extensions with `setup.py`) 

## Procedure

build a seed corpus of in-domain data, then:

iterate:
1. build language model
2. evaluate perplexity of unlabeled sents under this model
3. add *n* sents under the perplexity threshhold to the corpus

terminate when no new sentences are under the threshhold

## Results

see the jupyter notebooks for demos of selecting Jane Austen sentences from a mixture of sentences from Austen, Lewis Carroll and Herman Melville

## Resources

For KenLM:
https://yidatao.github.io/2017-05-31/kenlm-ngram/
http://victor.chahuneau.fr/notes/2012/07/03/kenlm.html
