## Synthetic datasets for NER task for under-resourced languages 

This repo contains primarily datasets described in the paper [Applying Natural Annotation and Curriculum Learning to Named Entity Recognition for Under-Resourced Languages (V. Lobov, A. Ivoylova, S. Sharoff, COLING 2022)](https://aclanthology.org/2022.coling-1.394/). The scripts contained here are for demonstration purposes. Please cite our paper if you wish to use these datasets in your work:

    @inproceedings{lobov-etal-2022-applying,
      title = "Applying Natural Annotation and Curriculum Learning to Named Entity Recognition for Under-Resourced Languages",
      author = "Lobov, Valeriy  and
        Ivoylova, Alexandra  and
        Sharoff, Serge",
      booktitle = "Proceedings of the 29th International Conference on Computational Linguistics",
      month = oct,
      year = "2022",
      address = "Gyeongju, Republic of Korea",
      publisher = "International Committee on Computational Linguistics",
      url = "https://aclanthology.org/2022.coling-1.394",
      pages = "4468--4480",
      abstract = "Current practices in building new NLP models for low-resourced languages rely either on Machine Translation of training sets from better resourced languages or on cross-lingual transfer from them. Still we can see a considerable performance gap between the models originally trained within better resourced languages and the models transferred from them. In this study we test the possibility of (1) using natural annotation to build synthetic training sets from resources not initially designed for the target downstream task and (2) employing curriculum learning methods to select the most suitable examples from synthetic training sets. We test this hypothesis across seven Slavic languages and across three curriculum learning strategies on Named Entity Recognition as the downstream task. We also test the possibility of fine-tuning the synthetic resources to reflect linguistic properties, such as the grammatical case and gender, both of which are important for the Slavic languages. We demonstrate the possibility to achieve the mean F1 score of 0.78 across the three basic entities types for Belarusian starting from zero resources in comparison to the baseline of 0.63 using the zero-shot transfer from English. For comparison, the English model trained on the original set achieves the mean F1-score of 0.75. The experimental results are available from https://github.com/ValeraLobov/SlavNER",
  }

#### Languages

There are seven languages:

- Western Slavonic:
  - Czech
  - Polish
- Southern Slavonic:
  - Bulgarian
  - Slovenian
- Eastern Slavonic:
  - Belarusian
  - Russian
  - Ukrainian

#### Dataset types and sizes

S1: a fully parallel dataset where the contexts do not take into account morphological features of the entities

S1 (there are quantities of entities and contexts divided by \ )

 LANG	| PER\context |	LOC\context |	ORG\context |	PRO\context |	EVT\context |
| --- | --- | --- | --- | --- | --- |
|RU|4492\7439|	1709\2904|	239\348|	- |	- |
|BE|	4492\7439|	1709\2904|	239\348	| 	- | -|
|BG|	4492\7439	|1709\2904|	239\348|	-  |	-  |
|CS	|4492\7439|	1709\2904	|239\348	| -	 | -|
|PL|	4492\7439	|1709\2904	|239\348	|  -	|-  |
|SL|	4492\7439	|1709\2904|	239\348|	 - |	-  |
|UK|	4492\7439	|1709\2904|	239\348|	-  |	-  |

S2: The same as S1, but takes morphological features into account

S2

 LANG	| PER\context |	LOC\context |	ORG\context |	PRO\context |	EVT\context |
 | --- | --- | --- | --- | --- | --- |
|RU	|4492\7439|	1709\2904|	239\348|	 -|	 -|
|BE|	4492\7439	|1709\2904|	239\348	 |-	 |-|
|BG|	4492\7439|	1709\2904	|239\348|	 -	 |-|
|CS|	4492\7439|	1709\2904	|239\348	| -	 |-|
|PL	|4492\7439	|1709\2904|	239\348	 |-	| -|
|SL	|4492\7439|	1709\2904	|239\348|	 -	| -|
|UK	|4492\7439|	1709\2904|	239\348|	 -	| -|

S3: not completely parallel, extensively big. Contains different entities for the languages

RU = 154 823 174 

BE = 152 098 065 

BG = 153 327 462 

CS = 154 823 174 

PL = 153 736 174 

SL = 152 513 299 

UK = 154 329 676 

S3

 LANG	| PER\context |	LOC\context |	ORG\context |	PRO\context |	EVT\context |
 | --- | --- | --- | --- | --- | --- |
|RU	|20000\7439|	1709\2904	|3000\1087|	50\50	|30\30|
|BE	|20000\7439	|1709\2904	|493\1087	|50\50|	30\30|
|BG	|20000\7439|	1709\2904	|1624\1087|	50\50|	30\30|
|CS|20000\7439|	1709\2904|	3000\1087	|50\50|	30\30|
|PL|	20000\7439	|1709\2904	|2000\1087	|50\50|	30\30|
|SL|	20000\7439	|1709\2904|	875\1087|	50\50	|30\30|
|UK	|20000\7439	|1709\2904	|2546\1087|	50\50	|30\30|
