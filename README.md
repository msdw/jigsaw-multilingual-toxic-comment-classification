# 22 nd Polyglot solution 

## PB score timeline
Ensemble Gmean of top score public submissions -> 0.9473 (8 June)
Ensemble LGBM solution and Gmean submission -> 0.9478 (10 June)
(Magic) Add external data to validate dataset and change to validate by language in second step training of XLM and ensemble by language -> 0.9500 (21 June)
Unfortunately, we boosted the score to 0.9500 in the last 2 days but no more TPU left to train new external data.

## Validate Dataset
We separated validate data to 3 set by language and find another 3 languages from external data to use in second step training in @riblidezso notebook. The out of fold score looks promising so we blend them to our main submission and boost the score to 0.9500.

## References
- Gmean notebook: https://www.kaggle.com/paulorzp/gmean-of-low-correlation-lb-0-952x
- XLM-Roberta: https://www.kaggle.com/riblidezso/train-from-mlm-finetuned-xlm-roberta-large
- LGBM solution: https://www.kaggle.com/miklgr500/lgbm-solution
- External data: https://www.kaggle.com/blackmoon/russian-language-toxic-comments , https://www.kaggle.com/shonenkov/open-subtitles-toxic-pseudo-labeling
- (Magic) Validate and fine-tuned by language: https://www.kaggle.com/medrau/train-from-mlm-finetuned-val-per-lang