# Cell Rangerの準備

## Cell Rangerとは
シングルセルから取得されたリードを参照配列にマッピングし、発現量を定量化する  

## 参考サイト
[10x GENOMICS Cell Range](https://www.10xgenomics.com/support/jp/software/cell-ranger/latest)

## 事前準備
```
mkdir ~/app
cd ~/app
```

## Cell Rangerのダウンロード(LINUX用)
```
curl -o cellranger-9.0.1.tar.gz "https://cf.10xgenomics.com/releases/cell-exp/cellranger-9.0.1.tar.gz?Expires=1743524942&Key-Pair-Id=APKAI7S6A5RYOXBWRPDA&Signature=gFgSNAkC21n7TVbG879IhhgWOTCP-ZSUj5bDxkOa1sc9jRI03i6WPYIz9gsqHuO9fKgRxTiQBS8FD8m5qfQB~DSvZe~Agay5pmoWBT8OM6q-Hibw9JJ7HQZ2g0kwqROR8V1VKtoymOeLRONleFwIT4OhPSCcY3XH3S6iROhwJVcdMYZKY4rQ0oTWkSSNwJN-LQbFgMFWSWQNUrmY0fEMupPsMbzxLuLA0B00SlPtl8yiaTcv4v8gWVipbH7yTAO5N1ZNzmsUnsR1blyL~AOmEMnZkVrrLlfe7F8Z5L9Ai4uVKhpQ~phdL7fKk~CzyzKfjpM0MTHpz9qJF73zKpkaHg__"
```

## 参照配列のダウンロード（mouse: GRCm39）
```
curl -O "https://cf.10xgenomics.com/supp/cell-exp/refdata-gex-GRCm39-2024-A.tar.gz"
```

## ファイルの解凍
```
tar -xvf cellranger-9.0.1.tar.gz
tar -xvf refdata-gex-GRCm39-2024-A.tar.gz
```

## 環境変数の設定
```
echo "export PATH=~/app/cellranger-x.y.z:$PATH" >> ~/.bashrc
```

## ディレクトリの設置
fastq/には各サンプルのFASTQファイルを、ref/にはマウスの参照配列を保存  
```
mkdir fastq # FASTQファイル保存用のディレクトリ
mkdir ref # 参照配列保存用のディレクトリ
```

