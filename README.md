# TF-Transcrptional-factors-with-multi-head-attention-layer-
classification of TFs Vs Non-TFs
Designed and trained a novel ATG-anchored Multi-Head Self-Attention deep learning architecture (Embedding + Conv1D + Self-Attention + MLP) in PyTorch to classify transcription factor (TF) vs. non-TF protein sequences, achieving 92.3% ROC-AUC, 86.5% accuracy, and 0.856 F1-score on a held-out test set of 251 sequences.

Implemented a 5-stage automated model validation framework (performance thresholds, class-recall gap analysis, overfitting diagnostics, sanity testing on known sequences, and random-baseline comparison) to rigorously confirm model reliability before reporting results.

More technical

Combined Conv1D motif extraction (capturing local sequence patterns e.g. zinc-finger, helix-turn-helix motifs) with multi-head self-attention for long-range residue dependencies, using residual connections and LayerNorm for stable training.
Optimized training using AdamW with OneCycleLR scheduling and gradient clipping; monitored train/validation loss, AUC, and F1 across epochs to select the best-performing checkpoint (Val AUC = 0.906).


