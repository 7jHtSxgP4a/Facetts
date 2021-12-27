## facetts
* An algorithm for estimating the cardinality in inner product spaces

## Environment
* Linux OS (Ubuntu)
* g++ 5.5.0 (or newer version)

## How to use
* Datasets
    * Creast your datasets from, e.g., rating data, by using Matrix Factorization (https://www.csie.ntu.edu.tw/~cjlin/libmf/).
    * Place your datasets at ``dataset`` directory.
        * 例　../dataset/netflix_mf-50.txt
    * 実際のカーディナリティはexact ディレクトに置く．
        * 例　../exact/netflix/netflix_thr4.csv
        * ファイルの各行：クエリid，実際のカーディナリティ
* 実行結果はcsv形式で出力する．
    * 結果の各行： クエリid，実際のカーディナリティ，推定したカーディナリティ，相対誤差，オンラインの実行時間
* パラメータはprameterディレクトリにあるthreshold.txt,   sampling_number.txtから読み込む.
* コンパイル：g++ -O3  -o facetts.out facetts.cpp -std=c++11
* 実行：./facetts.out
