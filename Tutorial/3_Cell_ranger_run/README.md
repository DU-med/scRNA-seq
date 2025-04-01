# Cell Rangerの実行

## Cell Rangerの実行コマンド
```
cellranger count \
  --id=CRR1297183 \ # サンプル名
  --transcriptome=ref/refdata-gex-GRCm39-2024-A \ # 参照配列の指定
  --fastqs=fastq/ \ # FASTQファイルがあるディレクトリの指定
  --sample=CRR1297183 \ # サンプルのFASTQファイルのID
  --expect-cells=10000 \ # おおよその細胞数
  --create-bam false # 中間ファイルのbamファイルを作成しない
```
