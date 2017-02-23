# Detailed steps to deploy RISE

RISE aims for the easy implementation of Information Retrieval models and the automation of evaluation.

Please cite the following paper if your are using it someway...

```
@inproceedings{Yang:2016:RSI:2970398.2970415,
 author = {Yang, Peilin and Fang, Hui},
 title = {A Reproducibility Study of Information Retrieval Models},
 booktitle = {Proceedings of the 2016 ACM International Conference on the Theory of Information Retrieval},
 series = {ICTIR '16},
 year = {2016},
 isbn = {978-1-4503-4497-5},
 location = {Newark, Delaware, USA},
 pages = {77--86},
 numpages = {10},
 url = {http://doi.acm.org/10.1145/2970398.2970415},
 doi = {10.1145/2970398.2970415},
 acmid = {2970415},
 publisher = {ACM},
 address = {New York, NY, USA},
 keywords = {evaluation system, ranking models, reproduciblity},
} 

```

1. `git clone https://github.com/Peilin-Yang/reproducibleIR.git`
2. Download the indexes, queries and evaluation files.
```bash
wget https://s3.amazonaws.com/virlab/rise.tar.gz
tar xvfz rise.tar.gz
``` 
Move all the folders (index, queries, judgments) to `$RISE_FILES`
3. open `$RISE_ROOT/docker/` 
