## facetts
* 内積空間におけるカーディナリティを推定するためのアルゴリズム

## 環境
* Linux OS(Ubuntu)
* g++ 5.5.0

## 使い方
* データセット
    * rating data からMF（Matrix Factorization）（https://www.csie.ntu.edu.tw/~cjlin/libmf/ ）により作成する．
    * データセットはdataset ディレクトリに置く．
        * 例　../dataset/netflix_mf-50.txt
    * 実際のカーディナリティはexact ディレクトに置く．
        * 例　../exact/netflix/netflix_thr4.csv
        * ファイルの各行：クエリid，実際のカーディナリティ
* 実行結果はcsv形式で出力する．
    * 結果の各行： クエリid，実際のカーディナリティ，推定したカーディナリティ，相対誤差，オンラインの実行時間
* パラメータはprameterディレクトリにあるthreshold.txt,   sampling_number.txtから読み込む.
* コンパイル：g++ -O3  -o facetts.out facetts.cpp -std=c++11
* 実行：./facetts.out
