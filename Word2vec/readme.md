# Word2Vec README

## Paper Reference
- Title: Efficient Estimation of Word Representations in Vector Space
- Authors: Mikolov et al. (2013)
- Link: https://arxiv.org/abs/1301.3781

## Overview
- Purpose: Efficient generation of high-quality word embeddings from massive text corpora.
- Contribution: Introduced CBOW and Skip‑Gram architectures + training optimizations.

## Model Architectures
### CBOW
- Predicts target word from averaged context embeddings.

### Skip‑Gram
- Predicts context words from a target word embedding.

## Training Techniques
- Hierarchical Softmax: Tree-based probability calculation.
- Negative Sampling: Approximate training via negative context examples.
- Subsampling: Discourage overfitting to frequent words.
- Dynamic window size: Random variation of context window.

## Benefits
- Fast training on large datasets.
- Better performance for rare word representations.
- Embeddings capture semantics effectively.

## Learning Path
1. Understand CBOW and Skip‑Gram.
2. Dive into softmax, hierarchical softmax, and negative sampling.
3. Explore subsampling and dynamic window strategies.
4. Learn how embeddings arise from trained weight matrices.
