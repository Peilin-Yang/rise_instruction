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

### Prerequisites
-----------------
* docker
* docker-compose


###Installation
-------------
1. `git clone https://github.com/Peilin-Yang/reproducibleIR.git`

2. Download the indexes, queries and evaluation files.
    ```
    wget https://s3.amazonaws.com/virlab/rise.tar.gz
    tar xvfz rise.tar.gz
    ```

3. Move the extracted folders (index, queries, judgments) to `$RISE_FILES`

4. open `$RISE_ROOT/docker/docker-compose.yml` change the paths to whatever applies

5. open `$RISE_ROOT/daemon/cronjobs` change the paths to whatever applies

6. go to `$RISE_ROOT/docker` and run
  ```shell
  docker-compose up -d
  ```
  _NOTICE: if the version of your docker is different from `1.21` then you can run `export COMPOSE_API_VERSION=1.18`_


###Utils
-------------
* Get Into the Running Docker Container
  `docker exec -i -t web /bin/bash`
* PHPMYADMIN_ALIAS `dba`

* db
  * user: `admin`
  * password: _by looking the docker log `docker logs web`_
