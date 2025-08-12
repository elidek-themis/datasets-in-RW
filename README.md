# Bias Evaluation Datasets

This document provides details for various datasets used for evaluating bias in language models that are available in the related work.

## Counterfactual Inputs Datasets

### Masked Tokens
| Dataset | Size | Bias Type | Metric |
| --- | --- | --- | --- |
| WinoGender | 720 | gender | Coref |
| WinoBias | 3,160 | gender | Coref |
| WinoBias+ | 1,367 | gender | Coref |
| GAP | 8,908 | gender | OverallF1, Bias Score (FemF1 / MascF1) |
| GAP-Subjective | - | gender | OverallF1, Bias Score |
| BUG | 108,419 | gender | Accuracy (F1), Population Bias (ΔG), Historical Bias (ΔS) |
| StereoSet | 16,995 | gender, race, profession, religion | lms, ss, iCAT |
| BEC-Pro | 5,400 | gender | Log likelihood |

### Unmasked Sentences
| Dataset | Size | Bias Type | Metric |
| --- | --- | --- | --- |
| CrowS-Pairs | 1,508 | age, disability, gender, nationality, physical appearance, race, religion, sexual orientation, socioeconomic status | Pseudo-log-likelihood |
| WinoQueer | 45,540 | sexual orientation | Modified pseudo-log-likelihood |
| RedditBias | 11,873 | gender, race, religion, sexual orientation | Pseudo-log-likelihood |
| Bias-STS-B | 16,980 | gender | Pearson correlation |
| PANDA | 98,583 | age, gender, race | Pseudo-log-likelihood |
| Equity Evaluation Corpus (EEC) | 4,320 | gender, religion | Pseudo-log-likelihood |
| Bias-NLI | 5,712,066 | gender, nationality, race | Net Neutral, Fraction Neutral, Threshold-based |

## Generative Datasets

### Sentence Completion
| Dataset | Size | Bias Type | Metric |
| --- | --- | --- | --- |
| Real Toxicity Prompts | 100,000 | disability, gender, nationality, physical appearance, race, religion, sexual orientation, cultural | Expected Max Toxicity, Toxicity Probability |
| BOLD | 23,679 | gender, race, religion, political ideology | Sentiment, Toxicity, Regard, Emotion, Gender Polarity |
| HolisticBias | 460,000 | age, disability, gender, nationality, physical appearance, race, religion, cultural, sexual orientation, socioeconomic status | Token Likelihood Bias, Generation Bias, Offensiveness Bias |
| TrustGPT | 9 | gender, race, religion | Toxicity, Bias, Value-Alignment |
| HONEST | 420 | gender | HONEST score |

### Question-Answering
| Dataset | Size | Bias Type | Metric |
| --- | --- | --- | --- |
| BBQ | 58,492 | age, disability, gender, nationality, physical appearance, race, religion, sexual orientation, socioeconomic status | Accuracy, sDIS, sAMB |
| UnQover | - | gender, nationality, religion, sexual orientation | Bias Score, Comparative Bias Score, Subject-Attribute Bias, Model Bias Intensity, Count-Based Metric |
