## Synthetic datasets for NER task for under-resourced languages 

This repo contains primarily datasets described in the paper Applying Natural Annotation and Curriculum Learning to Named Entity Recognition for Under-Resourced Languages (V. Lobov, A. Ivoylova, S. Sharoff, COLING 2022). The scripts contained here are for demonstration purposes. Please cite our paper if you wish to use these datasets in your work.

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
