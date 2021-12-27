## facetts
* An algorithm for estimating the cardinality in inner product spaces

## Environment
* Linux OS (Ubuntu)
* g++ 5.5.0 (or newer version)

## How to use
* Datasets
    * Creast your datasets from, e.g., rating data, by using Matrix Factorization (https://www.csie.ntu.edu.tw/~cjlin/libmf/).
    * Place your datasets at ``dataset`` directory.
        * Ex.)　../dataset/netflix_mf-50.txt
    * If you want to test accuracy, the ground truth datasets have to be at ``exact`` directory．
        * Ex.)　../exact/netflix/netflix_thr4.csv
        * Each line is ``id, cardinality``
* Test result is obtained by a csv file.
    * Each line consists of ``query id, real cardinality, estimated cardinality, error, running time``
* パラメータはprameterディレクトリにあるthreshold.txt,   sampling_number.txtから読み込む.
* Compile: ``g++ -O3 -o facetts.out facetts.cpp -std=c++11``
* Run: ``./facetts.out``
