# Cell Rangerの実行

## FASTQファイル名の変更
cell rangerを実行する際は、FASTQファイル名を特定のフォーマットにする必要あり
```
mv CRR1297183_f1.fastq.gz CRR1297183_S1_L001_R1_001.fastq.gz
mv CRR1297183_r2.fastq.gz CRR1297183_S1_L001_R2_001.fastq.gz
mv CRR1297184_f1.fastq.gz CRR1297184_S1_L001_R1_001.fastq.gz
mv CRR1297184_r2.fastq.gz CRR1297184_S1_L001_R2_001.fastq.gz
mv CRR1297185_r1.fastq.gz CRR1297185_S1_L001_R1_001.fastq.gz
mv CRR1297185_r2.fastq.gz CRR1297185_S1_L001_R2_001.fastq.gz
mv CRR1297186_r1.fastq.gz CRR1297186_S1_L001_R1_001.fastq.gz
mv CRR1297186_r2.fastq.gz CRR1297186_S1_L001_R2_001.fastq.gz
```

## Cell Rangerの実行コマンド
cellranger count \  
  --id=CRR1297183 \ # サンプル名  
  --transcriptome=ref/refdata-gex-GRCm39-2024-A \ # 参照配列の指定  
  --fastqs=fastq/ \ # FASTQファイルがあるディレクトリの指定  
  --sample=CRR1297183 \ # サンプルのFASTQファイルのID  
  --expect-cells=10000 \ # おおよその細胞数  
  --create-bam false # 中間ファイルのbamファイルを作成しない  
```
