# rumen_16s_rRNA_seq_profiling


## Importing Data


```

qiime tools import \
--type 'SampleData[PairedEndSequencesWithQuality]' \
--input---input-path casava-18-paired-end-demultiplexed \
--input-format CasavaOneEightSingleLanePerSampleDirFmt \
--output-path casava_pe_demux.qza \

```


결과로 Qiime2 에서 casava_pe_demux.qza 파일을 얻을수 있다.

## Visualization of importing data.
'''

qiime demux summarize \
--i-data casava_pe_demux.qza \
--o-visualization casava_pe_demux.qzv

'''

결과로는 casava_pe_demux.qzv파일을 얻을수 있다.

## Denoising with DADA2.
'''

qiime dada2 denoise-paired \
--i-demultiplexed-seqs casava_pe_demux.qza \
--p-trim-left-f 0 \
--p-trim-left-r 0 \
--p-trunc-len-f 291 \
--p-trunc-len-r 242 \
--o-table table-dada2.qza \
--o-representative-sequences rep-seqs.qza \
--o-denoising-stats stats-dada2.qza

'''

결과로  
1) table-dada2.qza
2) rep-seqs.qza
3) stats-dada2.qza 파일을 얻을수 있다.

## QC Summary파일 Visualization.
'''

qiime metadata tabulate \
--m-input-file stats-dada2.qza \
--o-visualization stas-dada2.qzv

'''

결과로 

4) stats-dada2.qzv를 얻을수 있다.

## Feature Table and Feature Data Summaries. 
'''

qiime feature-table summarize \
--i-table table-dada2.qza \
--o-visualization table-dada2.qzv \
--m-sample-metadata-file sample-metadata_ata.tsv

'''

결과로 table-dada2.qzv파일을 얻어야한다. 

-table-dada2.qzv 파일이 있어야지만 그래프와 같은 통계적 자료를 보면서 필터링의 기준을 정할수 있다.

**하지만**,,, 아래와 같은 오류가 나왔다.

There was an issue with loading the file sample-metadata.tsv as metadata:

  Metadata file path doesn't exist, or the path points to something other than a file. Please check that the path exists, has read permissions, and points to a regular file (not a directory): sample-metadata.tsv

  There may be more errors present in the metadata file. To get a full report, sample/feature metadata files can be validated with Keemei: https://keemei.qiime2.org

  Find details on QIIME 2 metadata requirements here: https://docs.qiime2.org/2023.5/tutorials/metadata/


  ## Representative Sequences 확인.
  '''

qiime feature-table tabulate-seqs \
--i-data rep-seqs.qza \
--o-visualization rep-seqs.qzv

'''

결과로

5) rep-seqs.qzv파일을 얻을수 있다. 
