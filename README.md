# rumen_16s_rRNA_seq_profiling

## Description

소(Cattle)와 같은 반추동물안에 있는 Microbiome에 대한 Microbiota들의 16S rRNA Sequence로 Taxonomy profiling을 하여 반추위내에서 메탄을 발생시키는 Microbiota들을 찾고
다양성 분석 및 계통분석을 통하여 메탄을 발생시키는 미생물들이 반추동물내에 얼마나 다양하게 분포하여있는지를 확인하고, 메탄 저감 물질을 처리하였을때 처리군과 대조군들과의 비교시 얼마나 효과가 있는지를 확인하기위하여 16S_rRNA 분석을 진행하였습니다. <br>

* 분석 Sample 개수 : 12개 Sample <br>
<br>

* 단어설명 <br>

**1. Microbiome, Microbiota** 이란?
![스크린샷 2024-03-10 22-43-47](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/e64fa4f5-23fc-4741-aa66-a8515b8d34d2) <br>
* **Microbiome**이란 Micro - 미생물 , Biome - 생태계로, "미생물 생태계" 라는 뜻으로 모든 미생물들과 단백질, 지질, 다당류, 핵산 및 microbiota의 대사물질을 포함합니다. <br>
* **Microbiota**는 Fungi, Bacteria, Archaea, Protists, Algae 들과 같은 각각의 미생물들을 지칭하는 단어로 사용 됩니다.
<br>

**2. 16S rRNA gene** : 16S rRNA는 원핵생물의 30S 리보솜 소단위체를 구성하는 성분으로(rRNA = ribosomal RNA 입니다.) 리보솜에서 단백질 번역과정에 중요한 역할을 하며 단백질 합성에 참여합니다. <br>

**"즉, 원핵세포의 Central Dogma에 참여하는 16S rRNA는 원핵생물에 있어 생명 유지를 위한 필수 기능을 수행하는 것에 참여하는 것이고, 생명유지를 하기위해 사용되는 것들은 거의 변화 없이 잘 보존된 부위 입니다. 그러한 의미에서 16S rRNA gene에 있는 유전 서열 영역중 Conserved region 은 보존적인 영역이 있다는 의미이고, 그래서 이 부분의 염기서열 분석으로 다양성분석 및 계통학적 분류가 가능합니다."** <br>
![image](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/c1755eb3-be94-4e74-ad48-012e6725a5ba)
<br> 
 * 1. conserved region(보존영역): 16S rRNA sequencing 분석에서 원핵생물인지 판별하기 위해 사용되는 서열입니다. <br>
 * 2. variable region(변이영역): 미생물마다 다른 부분이 있으므로 미생물의 종(species)을 구분하기 위한 서열입니다. <br>
* **variable region 각각을 "V1 ~ V9"라고 하는데 그 중 "V3 ~ V4" region, 혹은 "V4"가 16S rRNA sequencing에 통상적으로 사용됩니다.** 
![image](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/6e19da31-544f-4c4a-ba2b-8992ed9f5f5d) <br>
아래 두개의 논문 및 제조사 권장사항에서 V3 ~ V4 region이 16S rRNA Sequencing분석에 적합하다는 내용에 따라, 본 분석에서는 V3 ~ V4 region을 16S rRNA sequencing 분석에 사용하였습니다. <br>

* 참고문헌
* 1. Introduction 7~9번째 줄 참고. <br>
https://support.illumina.com/documents/documentation/chemistry_documentation/16s/16s-metagenomic-library-prep-guide-15044223-b.pdf <br>
* 2. Materials and Methods 8~9번째 줄 참고. <br>
https://synapse.koreamed.org/upload/synapsedata/pdfdata/1105acm/acm-23-1.pdf <br>
* 3. 마이크로바이옴의 연구 방법 3번째문단의 3~5번째줄 참고. <br>
http://www.btnews.or.kr/bbs/board.php?bo_table=bt_news&wr_id=139 <br>
* 4. 16S rRNA 유전자의 V3-V4 초가변 영역 앰플리콘을 이용한 현장 규모 혐기성 소화조 분석에서 한국의 현장 혐기성 소화조의 매우 다양한 원핵 미생물군과 미생물 조성의 미미한 계절 변동 및 기질 유형에 따른 상당한 차이 발견되었습니다.
     김후. (2023). Prokaryotic metataxonomics for analysis of field-scale anaerobic digesters and fecal microbiome (Doctoral dissertation, 한양대학교). <br>
* Illumina Sequencing Machine <br>
![스크린샷 2024-03-13 20-24-26](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/61bf425b-bc3a-49de-b453-d372845b5f50) <br>
 <br>

  * MiSeq은 짧은 DNA(150bp)에서 많은 DNA을 시퀀싱할 수 있고 HiSeq은 분석 가능한 길이가 비교적 긴편이나 (150~300bp) 그렇게 많은 DNA를 시퀀싱할 수는 없다는 차이가 있습니다.
  * 이러한 이유로 가격적인 부분에서 차이가 생기는데 MiSeq이 HiSeq에 비해 저렴합니다.
![스크린샷 2024-03-13 20-29-39](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/ef71a7c8-9279-4371-a219-f66254b19f9b) <br>
  * 용도별로 말하자면 Hiseq는 whole genome sequencing이나 functional metagenomics용으로 사용하고 miseq는 미생물 생태분석용으로 사용합니다.
<br>

## 16S rRNA Sequencing Analysis Pipeline   
![image](https://github.com/yoonseok95/rumen_16s_rRNA_seq_profiling/assets/145320727/5c1a7d5c-48fe-4dc8-8cb4-774faf19d017)   

## 1. Sampling
샘플링 Pipline : <br>
![image](https://github.com/yoonseok95/rumen_16s_rRNA_seq_profiling/assets/145320727/5f797e57-3cc8-418b-afa4-acc64dab2488) <br>

## 2. Library Construction and Sequencing <br>


## 3. Data Pre-processing <br>
Data Pre-processing Pipe line : <br>
![스크린샷 2024-03-13 21-30-24](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/9b261263-503b-461c-9816-6a33b2662ffb) <br>

### 3-1. Importing Data   
* QIIME2 에서는 모든 데이터를 .qza(Qiime 아티팩트) 형식으로 가져옵니다.
* Casava 1.8 demultiplexed Format은 아래 5가지 이름이 underscore로 연결된 파일명이며, Illumina Miseq으로 Paired-end 시퀀싱 시 일반적으로 연구자가 받게되는 파일명 형태 입니다.
  * 예) P129174h_S1_L001_R1_001.fastq.gz, P129174h_S1_L001_R2_001.fastq.gz

    i.sample identifier <br>
    ii.barcode sequence or a barcode identifier <br>
    iii.lane number <br>
    iv.direction of the read (i.e. R1 or R2) <br>
    v.set number <br>

* 실험 의뢰기관으로부터 받은 fastq 파일 이름이, 위와 같은 5개의 구분형태가 아니라면, 되도록 위와 같은 형태로 요구하여 받는게 튜토리얼을 따라가며 작업을 하는데에 도움이 됩니다.
    
    
```
qiime tools import \
--type 'SampleData[PairedEndSequencesWithQuality]' \
--input---input-path casava-18-paired-end-demultiplexed \
--input-format CasavaOneEightSingleLanePerSampleDirFmt \
--output-path casava_pe_demux.qza 
```
* output 파일 : **01) casava_pe_demux.qza** 생성 확인
* 데이터를 casava_pe_demux.qza 파일로 가져오면 이것을 Qiime2의 시각화 파일로 변환할수 있습니다.
**CasavaOneEightSingleLanePerSampleDirFmt** 은 정해져있는 단어로 '내가 이러한 인풋 형식으로 데이터를 집어넣을거야' 라는 의미의 코드입니다.

```
qiime demux summarize \
--i-data casava_pe_demux.qza \
--o-visualization casava_pe_demux.qzv
```
* output 파일 : **02) casava_pe_demux.qzv** 생성 확인 (모든 .qzv 형태의 파일 포멧은 QIIME2 Viewer에서 열수 있습니다.) <br>
* 위 .qzv 파일을 QIIME2 View에서 열기.
  * Overview : 샘플 데이터의 총 시퀀스(리드) 통계 및 샘플 별 시퀀스 수
  * Interactive Quality Plot : Forward와 Reverse Reads의 Quality scores를 Plot에서 확인하고, QC 단계의 조건들을 고민할수 있습니다.

QIIME2 View 링크:   

Demultiplexed Sequence counts summary :   
https://view.qiime2.org/visualization/?type=html&src=6dac8f63-0902-4743-bb6e-2cfed39375c8   

![스크린샷 2024-03-06 22-30-04](https://github.com/yoonseok95/rumen_16s_rRNA_seq_profiling/assets/145320727/6d6c0643-cd52-4d9d-9f8c-324862d4211c)   

Forward Reads와 Reverse Reads에 대한 Sequence별 Quality Score을 나타낸 그래프들은 다음과 같다.   

![스크린샷 2024-03-10 22-50-28](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/6ca35d76-bf56-4edf-a19a-6676798f357e)


그래프를 읽는 방법:

X축 : Sequence Base <br>
Y축 : Quality Score

를 의미하는것으로, 각 Sequence Base에서 Sample갯수들의 Quality Score의 분포를 박스플롯으로 그렸고 그 중앙값이 Median값이다.

* 박스플롯 확대/ 축소:
  
  마우스 왼쪽 클릭 한채로 원하는 Sequence Base에서 드래그 -> 확대
  빈공간에서 더블클릭 -> 축소 (원상복구)

* 제가 적용한 규칙은 Quality Score이 30 미만으로 떨어지는 지점까지 자르는 것이였습니다.

**위와같은 방법을 사용하여 다음 단계인 DADA2를 이용한 Denoising 단계에서의 노이즈 제거를 위한 매개변수 값을 결정할수 있다.**

### 3-2.Denoising with DADA2.   

* DADA2가 효율적으로 작동 하려면 Read Quality가 낮은 부분을 최대한 잘라내되, Foward(정방향) 과 Reverse(역방향)을 문제없이 병합할수 있도록 충분히 겹치는부분 (Merge 되는 부분)을 남겨 두는 것이 중요합니다.  
* 여기서는 12개의 샘플에 대해서 QIIME2에서 DADA2를 통해 Paired-end Alignment를 진행하여 높은 정확도로 키메라를 제거하면서 동시에 노이즈도 같이 잡아 내기위한 검사를 진행합니다.
  * casava_pe_demux.qzv 파일을 통해 직접 눈으로 보고 확인한 read quality를 기반으로 trimming과 truncation을 결정합니다.

    * --p-trim-left-f 과 --p-trim-left-r  : 5' 쪽에서 잘라낼때에 사용하는 Plugin <br>
    * --p-trunc-len-f 과 --p-trunc-len-r : 3' 쪽에서 잘라낼때에 사용하는 Plugin <br>

* truncation시, paired-end의 overlap 길이를 반드시 고려하여, 충분한 overlap이 유지되도록 주의를 요합니다. <br>
* 분석 파일은 2X150bp paired end 리드로서, V3-V4영역에 해당하는 염기들을 시퀀싱하였습니다.
  * read trimming을 전혀 하지 않아도 50bp오버랩. 최소 30bp 오버랩구간을 남기려면 현재 trimming 하는 Base Pair는 없고, truncation 하는 Base pair 들은 Forward 10 bp, Reverse 69bp 에 대하여 Truncation이 가능 합니다.
* 저는 제거된 데이터 상태에서 cleaned 한 Feature table을 얻는것 까지 진행 하였습니다. <br>

### 3-2-1. DADA2 실행

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
* Output 파일 1: **03) table-dada2.qza** 생성 확인
* Output 파일 2: **04) rep-seqs.qza** 생성 확인
* Output 파일 3: **05) stats-dada2.qza** 생성 확인
* 이 방법은 Paired-end 시퀀스의 잡음(noise)을 제거하고 복제를 해제한 후 필터링을 진행합니다.
* 각 명령에 대한 자세한 설명은 https://docs.qiime2.org/2021.2/plugins/available/dada2/denoise-paired/?highlight=denoise%20paired 에서 확인할수 있습니다.


### 3-2-2. QC Summary파일 Visualization.

```
qiime metadata tabulate \
--m-input-file stats-dada2.qza \
--o-visualization stas-dada2.qzv
```

* Output 파일: **06) stats-dada2.qzv** 생성 확인 <br>
* 위 .qzv 파일을 https://view.qiime2.org/ 에서 열기.
* 최초 raw data가 DADA2 작업후, 최종 어느정도 filtering되었는지 확인 가능
  * 샘플별 최초 시퀀스 리드수(input),QC로 filter된후 (filtered, denoised), Paired-end 시퀀스 merging후 (merged),
    Chimera 제거후 (non-chimeric)의 리드수 확인가능 합니다.
  * filtered reads 수가 너무 적게 남았거나 하면, trimming이나 truncation parameter 수를 조정하여 DADA2를 재 실행 해야합니다.


### 3-3. Feature Table and Feature Data Summaries. <br>
### 3-3-1. Feature Table Summary 파일만들기

```
qiime feature-table summarize \
--i-table table-dada2.qza \
--o-visualization table-dada2.qzv \
--m-sample-metadata-file sample-metadata_ata.tsv
```

정상적인 결과로는 table-dada2.qzv파일 생성을 확인할수 있습니다.

- table-dada2.qzv 파일이 있어야지만 그래프와 같은 통계적 자료를 보면서 필터링의 기준을 정할수 있다.

**하지만**,,, 아래와 같은 오류가 나왔다.

There was an issue with loading the file sample-metadata.tsv as metadata:

  Metadata file path doesn't exist, or the path points to something other than a file. Please check that the path exists, has read permissions, and points to a regular file (not a directory): sample-metadata.tsv

  There may be more errors present in the metadata file. To get a full report, sample/feature metadata files can be validated with Keemei: https://keemei.qiime2.org

  Find details on QIIME 2 metadata requirements here: https://docs.qiime2.org/2023.5/tutorials/metadata/


### 3-3-2. Representative Sequences 확인.

```
qiime feature-table tabulate-seqs \
--i-data rep-seqs.qza \
--o-visualization rep-seqs.qzv
```


결과로

* rep-seqs.qzv파일을 얻을수 있다.
* 위 .qzv 파일을 qiime2 view에서 열수 있다.

  * Sequence Length 통계 : ASVs 마다의 평균 시퀀스 length
  * Sequence Lenghs의 평균 분포
  * Sequence Table : Features의 실제 시퀀스 <br>

* rep-seqs.qzv 파일 Qiime2 View로 열기 : 
https://view.qiime2.org/visualization/?src=028fe789-c56d-4d14-98ce-0f304df29ab3&type=html
![스크린샷 2024-03-07 17-50-38](https://github.com/yoonseok95/rumen_16s_rRNA_seq_profiling/assets/145320727/baf8371a-eedb-4361-9a8f-c4245d8b9257) <br>
## 4. Diversity Analysis <br>
Diversity Analysis Pipeline : <br>
![스크린샷 2024-03-13 21-33-02](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/b41ac96f-6c87-41c5-a857-bfea54d116e8)

## 5. Taxonomy Profiling <br>
Taxonomy Profiling Pipeline : <br>
![스크린샷 2024-03-13 21-37-06](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/ea6c2704-7ab8-4558-ba16-5f9860f532e6) <br>
<br>
## 6. 결과도출 <br>
Conclusion Pipeline : <br>
![4 - Untitled slide](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/6ed6d2a0-7c8a-4743-a141-a0fc62ef6366)




