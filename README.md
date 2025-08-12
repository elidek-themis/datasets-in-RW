# Bias Evaluation Datasets

This document provides details for various datasets used for evaluating bias in language models that are available in the related work. The taxonomy is based on the work of Isabel O Gallegos et al. [“Bias and fairness in large language models: A survey”](https://arxiv.org/abs/2309.00770). In: arXiv preprint arXiv:2309.00770 (2023).

## Counterfactual Inputs Datasets

### Masked Tokens
| Dataset | Size | Bias Type | Metric | URL | Reference
| --- | --- | --- | --- | --- | --- |
| WinoGender | 720 | gender | Coref | https://github.com/rudinger/winogender-schemas| Rachel Rudinger et al. [Gender Bias in Coreference Resolution](https://arxiv.org/abs/1804.09301). 2018. arXiv: 1804 . 09301 [cs.CL].|
| WinoBias | 3,160 | gender | Coref | | Jieyu Zhao et al. [Gender Bias in Coreference Resolution: Evaluation and Debiasing Methods](https://arxiv.org/abs/1804.06876). 2018. arXiv: 1804.06876 [cs.CL].|
| WinoBias+ | 1,367 | gender | Coref | | Eva Vanmassenhove, Chris Emmery, and Dimitar Shterionov. [NeuTral Rewriter: A Rule-Based and Neural Approach to Automatic Rewriting into Gender-Neutral Alternatives](https://arxiv.org/abs/2109.06105). 2021. arXiv: 2109.06105 [cs.CL].|
| GAP | 8,908 | gender | OverallF1, Bias Score (FemF1 / MascF1) | | Kellie Webster et al. [Mind the GAP: A Balanced Corpus of Gendered Ambiguous Pronouns](https://arxiv.org/abs/1810.05201). 2018. arXiv: 1810.05201 [cs.CL].|
| GAP-Subjective | - | gender | OverallF1, Bias Score | | Kartikey Pant and Tanvi Dadu. [Incorporating Subjectivity into Gendered Ambiguous Pro-noun (GAP) Resolution using Style Transfer](https://aclanthology.org/2022.gebnlp-1.28/). In: Proceedings of the 4th Workshop on Gender Bias in Natural Language Processing (GeBNLP). Ed. by Christian Hardmeier et al. Seattle, Washington: Association for Computational Linguistics, July 2022, pp. 273–281. doi: 10.18653/v1/2022.gebnlp-1.28.|
| BUG | 108,419 | gender | Accuracy (F1), Population Bias (ΔG), Historical Bias (ΔS) | | Shahar Levy, Koren Lazar, and Gabriel Stanovsky. [Collecting a Large-Scale Gender Bias Dataset for Coreference Resolution and Machine Translation](https://arxiv.org/abs/2109.03858). 2021. arXiv: 2109.03858 [cs.CL].|
| StereoSet | 16,995 | gender, race, profession, religion | lms, ss, iCAT | | Moin Nadeem, Anna Bethke, and Siva Reddy. [StereoSet: Measuring stereotypical bias in pretrained language models](https://arxiv.org/abs/2004.09456.). 2020. arXiv: 2004.09456 [cs.CL].|
| BEC-Pro | 5,400 | gender | Log likelihood | | Marion Bartl, Malvina Nissim, and Albert Gatt. [Unmasking Contextual Stereotypes: Measuring and Mitigating BERT’s Gender Bias](https://arxiv.org/abs/2010.14534). 2020. arXiv: 2010.14534 [cs.CL].|

### Unmasked Sentences
| Dataset | Size | Bias Type | Metric |URL | Reference
| --- | --- | --- | --- | --- | --- |
| CrowS-Pairs | 1,508 | age, disability, gender, nationality, physical appearance, race, religion, sexual orientation, socioeconomic status | Pseudo-log-likelihood | |  Nikita Nangia et al. [CrowS-Pairs: A Challenge Dataset for Measuring Social Biases in Masked Language Models](https://arxiv.org/abs/2010.00133). 2020. arXiv: 2010.00133 [cs.CL]|
| WinoQueer | 45,540 | sexual orientation | Modified pseudo-log-likelihood | | Virginia K. Felkner et al. WinoQueer: [A Community-in-the-Loop Benchmark for Anti-LGBTQ+ Bias in Large Language Models](https://arxiv.org/abs/2306.15087). 2024. arXiv: 2306.15087 [cs.CL].|
| RedditBias | 11,873 | gender, race, religion, sexual orientation | Pseudo-log-likelihood || Soumya Barikeri et al. [RedditBias: A Real-World Resource for Bias Evaluation and Debiasing of Conversational Language Models](https://arxiv.org/abs/2106.03521). 2021. arXiv: 2106.03521 [cs.CL].|
| Bias-STS-B | 16,980 | gender | Pearson correlation | | Kellie Webster et al. [Measuring and Reducing Gendered Correlations in Pre-trained Models](https://arxiv.org/abs/2010.06032). 2021. arXiv: 2010.06032 [cs.CL].|
| PANDA | 98,583 | age, gender, race | Pseudo-log-likelihood || Rebecca Qian et al. [Perturbation Augmentation for Fairer NLP](https://arxiv.org/abs/2205.12586). 2022. arXiv: 2205.12586 [cs.CL].|
| Equity Evaluation Corpus (EEC) | 4,320 | gender, religion | Pseudo-log-likelihood || Svetlana Kiritchenko and Saif M. Mohammad. [Examining Gender and Race Bias in Two Hundred Sentiment Analysis Systems](https://arxiv.org/abs/1805.04508). 2018. arXiv: 1805.04508 [cs.CL].|
| Bias-NLI | 5,712,066 | gender, nationality, race | Net Neutral, Fraction Neutral, Threshold-based || Sunipa Dev et al. [On Measuring and Mitigating Biased Inferences of Word Embeddings](https://arxiv.org/abs/1908.09369). 2019. arXiv: 1908.09369 [cs.CL].|

## Generative Datasets

### Sentence Completion
| Dataset | Size | Bias Type | Metric | URL | Reference
| --- | --- | --- | --- | --- | --- |
| Real Toxicity Prompts | 100,000 | disability, gender, nationality, physical appearance, race, religion, sexual orientation, cultural | Expected Max Toxicity, Toxicity Probability || Samuel Gehman et al. [RealToxicityPrompts: Evaluating Neural Toxic Degeneration in Language Models](https://arxiv.org/abs/2009.11462). 2020. arXiv: 2009.11462 [cs.CL].|
| BOLD | 23,679 | gender, race, religion, political ideology | Sentiment, Toxicity, Regard, Emotion, Gender Polarity || Jwala Dhamala et al. [BOLD: Dataset and Metrics for Measuring Biases in Open-Ended Language Generation](http://dx.doi.org/10.1145/3442188.3445924). In: Proceedings of the 2021 ACM Conference on Fairness, Accountability, and Transparency. FAccT 21. ACM, Mar. 2021, pp. 862–872. doi: 10.1145/3442188.3445924.|
| HolisticBias | 460,000 | age, disability, gender, nationality, physical appearance, race, religion, cultural, sexual orientation, socioeconomic status | Token Likelihood Bias, Generation Bias, Offensiveness Bias || Eric Michael Smith et al. ["I’m sorry to hear that": Finding New Biases in Language Models with a Holistic Descriptor Dataset](https://arxiv.org/abs/2205.09209). 2022. arXiv: 2205.09209 [cs.CL].|
| TrustGPT | 9 | gender, race, religion | Toxicity, Bias, Value-Alignment || Yue Huang et al. [TrustGPT: A Benchmark for Trustworthy and Responsible Large Language Models](https://arxiv.org/abs/2306.11507). 2023. arXiv: 2306.11507 [cs.CL].|
| HONEST | 420 | gender | HONEST score || Debora Nozza, Federico Bianchi, and Dirk Hovy. [HONEST: Measuring Hurtful Sentence Completion in Language Models](https://aclanthology.org/2021.naacl-main.191/). In: Proceedings of the 2021 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies. Ed. by Kristina Toutanova et al. Online: Association for Computational Linguistics, June 2021, pp. 2398–2406. doi: 10.18653 / v1 / 2021 . naacl-main. 191.|

### Question-Answering
| Dataset | Size | Bias Type | Metric | URL | Reference
| --- | --- | --- | --- | --- | --- |
| BBQ | 58,492 | age, disability, gender, nationality, physical appearance, race, religion, sexual orientation, socioeconomic status | Accuracy, sDIS, sAMB || Alicia Parrish et al. [BBQ: A Hand-Built Bias Benchmark for Question Answering](https://arxiv.org/abs/2110.08193). 2022. arXiv: 2110.08193 [cs.CL].|
| UnQover | - | gender, nationality, religion, sexual orientation | Bias Score, Comparative Bias Score, Subject-Attribute Bias, Model Bias Intensity, Count-Based Metric || Tao Li et al. [UnQovering Stereotyping Biases via Underspecified Questions](https://arxiv.org/abs/2010.02428). 2020. arXiv: 2010.02428 [cs.CL].|
