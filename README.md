# Grammar Scoring Engine – Summary Report 

**Objective:** Predict continuous grammar proficiency scores (1–5) from spoken language transcripts using a rubric-based evaluation framework.


**Data:**

* Audio files (45–60 seconds) in .wav format.

* Training set includes grammar scores; test set has no labels.

**Audio to Text Conversion:**

* Speech audio was converted into text transcripts using an automatic speech recognition (ASR) pipeline.
* Generated transcripts were stored and reused to ensure consistent downstream processing.
 

**Preprocessing:**

  * Text normalization (lowercasing, whitespace cleanup).
  * Sentence and word tokenization using NLTK.
  * POS tagging for grammatical structure analysis.

**Feature Engineering:**

  * Sentence length and variability.
  * Word-level complexity.
  * POS-based grammatical indicators.
  * Fluency and self-correction cues.

**Model & Pipeline:**

  * Scikit-learn pipeline with a **tree-based regression model**.
  * Predictions clipped to the valid score range **[1, 5]**.

**Evaluation Metrics:**

  * Cross-validation RMSE
  * Training RMSE
  * Training Pearson correlation

**Visual Analysis:**

  * Actual vs Predicted scores
  * Error distribution and outliers
  * Residual analysis
  * Score-wise error breakdown
  * Test prediction distribution 

**Submission:**

  * Test predictions rounded and clipped to [1–5].
  * Saved in required `filename, label` format.

**Conclusion:**

  * The model is stable, interpretable, and rubric-aware.
  * Demonstrates reliable performance under limited data constraints and meets all mentioned requirements.

# === FINAL RESULTS ==

* CV RMSE: 0.7038 (+/- 0.0302)
* Training RMSE: 0.5017
* Training Pearson: 0.8376



