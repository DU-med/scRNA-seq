# scanpyを実施するための環境準備

## 1. 仮想環境の構築
```
mamba create -n scanpy python=3.12 -y
```

## 2. 仮想環境のアクティベート
```
mamba activate scanpy
```

## 3. 必要なライブラリのインストール
```
mamba install conda-forge::scanpy -y # scanpyのインストール
mamba install bioconda::harmonypy -y # サンプルデータ統合のためのライブラリ
mamba install jupyter nbclassic pandas matplotlib seaborn -y # その他諸々

## 4. jupyter notebookの起動
ポートは9000番を使用
```
jupyter nbclassic --port 9000
```
