# rumen_16s_rRNA_seq_profiling

### 목적
경제동물, 그중에서도 소(Cattle)와 같은 반추동물안에있는 Microbiome에 대한 Microbiota들의 16S rRNA Sequence로 Taxonomy profiling을 하여 반추위내에서 메탄을 발생시키는 Microbiota들을 찾고
다양성 분석을 통하여 메탄을 발생시키는 미생물들이 반추동물내에 얼마나 다양하게 분포하여있는지를 확인하고자 16S_rRNA 분석을 진행하였다.

### Why 16S rRNA?

### Pipeline

## Importing Data


```
qiime tools import \
--type 'SampleData[PairedEndSequencesWithQuality]' \
--input---input-path casava-18-paired-end-demultiplexed \
--input-format CasavaOneEightSingleLanePerSampleDirFmt \
--output-path casava_pe_demux.qza 
```
데이터를 casava_pe_demux.qza 파일로 가져오면 이것을 Qiime2의 시각화 파일로 변환할수 있다.

```
qiime demux summarize \
--i-data casava_pe_demux.qza \
--o-visualization casava_pe_demux.qzv
```

결과로 얻은 casava_pe_demux.qzv 파일은 https://view.qiime2.org/ 에 업로드하여 확인이 가능하다.

여기에서 다음과 같은 유용한 정보를 찾을수 있다.

QIIME2 View 링크:

https://view.qiime2.org/visualization/?type=html&src=6dac8f63-0902-4743-bb6e-2cfed39375c8 

![스크린샷 2024-03-06 22-30-04](https://github.com/yoonseok95/rumen_16s_rRNA_seq_profiling/assets/145320727/6d6c0643-cd52-4d9d-9f8c-324862d4211c)

Forward Reads와 Reverse Reads에 대한 Sequence별 Quality Score을 나타낸 그래프들은 다음과 같다.

![스크린샷 2024-03-06 22-33-26](https://github.com/yoonseok95/rumen_16s_rRNA_seq_profiling/assets/145320727/74499927-0300-4e34-a9b1-e16686d7b253)

그래프를 읽는 방법:

X축 : Quality Score

Y축 : Sequence Base

를 의미하는것으로, 각 Sequence Base에서 Sample갯수들의 Quality Score의 분포를 박스플롯으로 그렸고 그 중앙값이 Median값이다.

* 박스플롯 확대/ 축소:
  
  마우스 왼쪽 클릭 한채로 원하는 Sequence Base에서 드래그 -> 확대
  
  빈공간에서 더블클릭 -> 축소 (원상복구)

** 위와같은 방법을 사용하여 다음 단계인 DADA2를 이용한 Denoising 단계에서의 노이즈 제거를 위한 매개변수 값을 결정할수 있다. **

* 제가 적용한 규칙은 Quality Score이 30 미만으로 떨어지는 지점까지 자르는 것이였습니다.



## Denoising with DADA2.

```
qiime dada2 denoise-paired \
--i-demultiplexed-seqs casava_pe_demux.qza \
--p-trim-left-f 0 \
--p-trim-left-r 0 \
--p-trunc-len-f 291 \
--p-trunc-len-r 242 \
--o-table table-dada2.qza \
--o-representative-sequences rep-seqs.qza \
--o-denoising-stats stats-dada2.qza
```

결과로  
1) table-dada2.qza
2) rep-seqs.qza
3) stats-dada2.qza 파일을 얻을수 있다.

## QC Summary파일 Visualization.

```
qiime metadata tabulate \
--m-input-file stats-dada2.qza \
--o-visualization stas-dada2.qzv
```

결과로 

4) stats-dada2.qzv를 얻을수 있다.

## Feature Table and Feature Data Summaries. 

```
qiime feature-table summarize \
--i-table table-dada2.qza \
--o-visualization table-dada2.qzv \
--m-sample-metadata-file sample-metadata_ata.tsv
```

결과로 table-dada2.qzv파일을 얻어야한다. 

-table-dada2.qzv 파일이 있어야지만 그래프와 같은 통계적 자료를 보면서 필터링의 기준을 정할수 있다.

**하지만**,,, 아래와 같은 오류가 나왔다.

There was an issue with loading the file sample-metadata.tsv as metadata:

  Metadata file path doesn't exist, or the path points to something other than a file. Please check that the path exists, has read permissions, and points to a regular file (not a directory): sample-metadata.tsv

  There may be more errors present in the metadata file. To get a full report, sample/feature metadata files can be validated with Keemei: https://keemei.qiime2.org

  Find details on QIIME 2 metadata requirements here: https://docs.qiime2.org/2023.5/tutorials/metadata/


## Representative Sequences 확인.

```
qiime feature-table tabulate-seqs \
--i-data rep-seqs.qza \
--o-visualization rep-seqs.qzv
```


결과로

5) rep-seqs.qzv파일을 얻을수 있다. 
