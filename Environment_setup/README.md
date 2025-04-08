# scanpyを実施するための環境準備

## 1. 琉球大学サーバーへのSSH接続
```
ssh x3
```

## 2. 仮想環境の構築
```
mamba create -n scanpy python=3.12 -y
```

## 3. 仮想環境のアクティベート
```
mamba activate scanpy
```

## 4. 必要なライブラリのインストール
```
mamba install conda-forge::scanpy -y # scanpyのインストール
mamba install conda-forge::python-igraph -y
mamba install conda-forge::leidenalg -y
mamba install bioconda::harmonypy -y # サンプルデータ統合のためのライブラリ
mamba install jupyter nbclassic pandas matplotlib seaborn -y # その他諸々
```
## 5. jupyter notebookの起動
ポートは9000番を使用
```
jupyter nbclassic --port 9000
```

## 6. jupyter notebookの使い方
**参考動画**  
https://www.youtube.com/watch?v=J4_ijz15v_w  
https://www.youtube.com/watch?v=K75k-YCxVtw  
https://www.youtube.com/watch?v=ktKrUUelSY0  
