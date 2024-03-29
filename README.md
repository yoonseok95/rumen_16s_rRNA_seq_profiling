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

**2. 16S rRNA gene** : <br>
16S rRNA는 원핵생물의 30S 리보솜 소단위체를 구성하는 성분으로(rRNA = ribosomal RNA 입니다.) 리보솜에서 단백질 번역과정에 중요한 역할을 하며 단백질 합성에 참여합니다. <br>

**"즉, 원핵세포의 Central Dogma에 참여하는 16S rRNA는 원핵생물에 있어 생명 유지를 위한 필수 기능을 수행하는 것에 참여하는 것이고, 생명유지를 하기위해 사용되는 것들은 거의 변화 없이 잘 보존된 부위 입니다. 그러한 의미에서 16S rRNA gene에 있는 유전 서열 영역중 Conserved region 은 보존적인 영역이 있다는 의미이고, 그래서 이 부분의 염기서열 분석으로 다양성분석 및 계통학적 분류가 가능합니다."** <br>
![스크린샷 2024-03-14 11-10-29](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/bb7df671-44c6-4e62-9c3c-6c229c260243)
<br> 
 * 1. conserved region(보존영역): 16S rRNA sequencing 분석에서 원핵생물인지 판별하기 위해 사용되는 서열입니다. <br>
 * 2. variable region(변이영역): 미생물마다 다른 부분이 있으므로 미생물의 종(species)을 구분하기 위한 서열입니다. <br>
* **variable region 각각을 "V1 ~ V9"라고 하는데 그 중 "V3 ~ V4" region, 혹은 "V4"가 16S rRNA sequencing에 통상적으로 사용됩니다.** 
![image](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/6e19da31-544f-4c4a-ba2b-8992ed9f5f5d) <br>
아래 두개의 논문 및 제조사 권장사항에서 V3 ~ V4 region이 16S rRNA Sequencing분석에 적합하다는 내용에 따라, 본 분석에서는 V3 ~ V4 region을 16S rRNA sequencing 분석에 사용하였습니다. <br>

* 참고문헌 (분석할 유전자의 영역 선택에 있어 밴치마킹한 참고논문)
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
  * 그래서 Sample에 대한 Sequencing Data를 얻을때 Illumina사의 Miseq을 통해서 Data를 받았습니다.
<br>

## 16S rRNA Sequencing Analysis Pipeline   
![image](https://github.com/yoonseok95/rumen_16s_rRNA_seq_profiling/assets/145320727/5c1a7d5c-48fe-4dc8-8cb4-774faf19d017)   

## 1. Sampling
샘플링 Pipline : <br>
![image](https://github.com/yoonseok95/rumen_16s_rRNA_seq_profiling/assets/145320727/5f797e57-3cc8-418b-afa4-acc64dab2488) <br>

## 2. Library Construction and Sequencing <br>


## 3. Data Pre-processing <br>
Data Pre-processing Pipe line : <br>
<br>
![스크린샷 2024-03-13 21-30-24](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/9b261263-503b-461c-9816-6a33b2662ffb) <br>
* Data Pre-processing 과정에서의 분석 Tool : **Qiime2-2023.5** <br>
<br>

* Qiime2 분석 tool 내전체 Pipeline <br>
![image](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/01f36875-6ec6-447a-b2df-dc7ea0ae28cc) <br>
* QIIME2 에서는 모든 데이터를 .qza 형식(Qiime 아티팩트)으로 가져옵니다.
* Illumina Miseq으로 Paired-end 시퀀싱 시 일반적으로 연구자가 받게되는 파일명 형태는 demultiplexed paired-end 데이터셋 <br>
  (Casava 1.8 demultiplexed paired-end sequences)으로 Data Importing후 바로 Denoising 단계로 진행했습니다. <br>
* 데이터셋 형태가 Casava 형태인 이유는 Qiime2 tool에서 가장 잘 호환이 되는 형태의 데이터셋 이기때문입니다.
* Casava 1.8 demultiplexed Format은 아래 5가지 이름이 underscore로 연결된 파일명입니다.
  * 예) P129174h_S1_L001_R1_001.fastq.gz, P129174h_S1_L001_R2_001.fastq.gz

    i.sample identifier <br>
    ii.barcode sequence or a barcode identifier <br>
    iii.lane number <br>
    iv.direction of the read (i.e. R1 or R2) <br>
    v.set number <br>

* 실험 의뢰기관으로부터 받은 fastq 파일 이름이, 위와 같은 5개의 구분형태가 아니라면, 되도록 위와 같은 형태로 요구하여 받는게 Qiime2 를 활용하여 데이터 분석에 있어 효율적입니다. <br>
### 3-1. Importing Data   
    
```
qiime tools import \
--type 'SampleData[PairedEndSequencesWithQuality]' \ # [PairedEndSequencesWithQuality]는 Sample Data의 type을 설명
--input-path casava-18-paired-end-demultiplexed \ # 데이터를 Qiime에 Import 하는 경로 지정하는 코드
--input-format CasavaOneEightSingleLanePerSampleDirFmt \ # CasavaOneEightSingleLanePerSampleDirFmt 은 정해져있는 단어로 '내가 이러한 인풋 형식으로 데이터를 집어넣을거야' 라는 의미의 코드
--output-path casava_pe_demux.qza 
```
* output 파일 : **01) casava_pe_demux.qza** 생성 확인
* 데이터를 casava_pe_demux.qza 파일로 가져오면 이것을 Qiime2 view에 Drag and Drop으로 Qiime2의 시각화 파일로 변환할수 있습니다.

### 3-1-1. Visualizing with Imported Data

```
qiime demux summarize \ # plugin code : CasavaOneEightSingleLanePerSampleDirFmt 형식으로 demultiplexed된 output 파일을 요약
--i-data casava_pe_demux.qza \ # Data Importing단계에서 나온 output파일을 다시 Qiime2로 Import
--o-visualization casava_pe_demux.qzv # 결과로 Import 된 .qza 파일이 .qzv 로 바뀌면서 시각화 가능
```
* output 파일 : **02) casava_pe_demux.qzv** 생성 확인 (모든 .qzv 형태의 파일 포멧은 QIIME2 Viewer에서 열수 있습니다.) <br>
* 위 .qzv 파일을 QIIME2 View에 Drag and Drop으로 시각화
  * Overview : 샘플 데이터의 총 시퀀스(리드) 통계 및 샘플 별 시퀀스 수
  * Interactive Quality Plot : Forward와 Reverse Read 들의 Quality scores를 Plot에서 확인하고, QC 단계의 조건들을 고민할수 있습니다.
  * Illumina 사에서 MiSeq을 통해 Sequencing이 진행되는데, Sequencing이 진행되는 과정에서 발생되는 Error값, 혹은 Sample Read들이 너무 조금 읽힌경우 들에 한하여 그 값들을 잘라내어 분석 오차를 줄일수 있습니다.


QIIME2 View 링크:   

Demultiplexed Sequence counts summary :   
https://view.qiime2.org/visualization/?type=html&src=6dac8f63-0902-4743-bb6e-2cfed39375c8   

![스크린샷 2024-03-06 22-30-04](https://github.com/yoonseok95/rumen_16s_rRNA_seq_profiling/assets/145320727/6d6c0643-cd52-4d9d-9f8c-324862d4211c)   

Forward Reads와 Reverse Reads에 대한 Sequence별 Quality Score을 나타낸 그래프들은 다음과 같습니다.   

![스크린샷 2024-03-10 22-50-28](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/6ca35d76-bf56-4edf-a19a-6676798f357e)


그래프를 읽는 방법:

X축 : Sequence Base <br>
Y축 : Quality Score

를 의미하는것으로, 각 Sequence Base에서 Sample갯수들의 Quality Score의 분포를 박스플롯으로 그렸고 그 중앙값이 Median값이다.

* 박스플롯 확대/ 축소:
  
  마우스 왼쪽 클릭 한채로 원하는 Sequence Base에서 드래그 -> 확대
  빈공간에서 더블클릭 -> 축소 (원상복구)

* trimming 및 truncation을 진행하기위해 기준으로 삼은것은 각 Boxplot 에서의 Median 값이 30이 안되는 Sequence Base들을 잘라내었다. 

**위와같은 방법을 사용하여 다음 단계인 DADA2를 이용한 Denoising 단계에서의 노이즈 제거를 위한 매개변수 값을 결정할수 있다.**

### 3-2.Denoising with DADA2.   

* DADA2가 효율적으로 작동 하려면 Read Quality가 낮은 부분을 최대한 잘라내되, Foward(정방향) 과 Reverse(역방향)을 문제없이 병합할수 있도록 충분히 겹치는부분 (Merge 되는 부분)을 남겨 두는 것이 중요합니다.  
* 여기서는 12개의 샘플에 대해서 QIIME2에서 DADA2를 통해 Paired-end Alignment를 진행하여 높은 정확도로 키메라를 제거하면서 동시에 노이즈도 같이 잡아 내기위한 검사를 진행합니다.
  * casava_pe_demux.qzv 파일을 통해 직접 눈으로 보고 확인한 read quality를 기반으로 trimming과 truncation을 결정합니다.

    * **--p-trim-left-f 과 --p-trim-left-r  : 5' 쪽에서 잘라낼때에 사용하는 Plugin** <br>
    * **--p-trunc-len-f 과 --p-trunc-len-r : 3' 쪽에서 잘라낼때에 사용하는 Plugin** <br>

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
<br>
* 메타데이터가 없다는 내용의 오류코드
```
There was an issue with loading the file sample-metadata.tsv as metadata:

  Metadata file path doesn't exist, or the path points to something other than a file. Please check that the path exists, has read permissions, and points to a regular file (not a directory): sample-metadata.tsv

  There may be more errors present in the metadata file. To get a full report, sample/feature metadata files can be validated with Keemei: https://keemei.qiime2.org

  Find details on QIIME 2 metadata requirements here: https://docs.qiime2.org/2023.5/tutorials/metadata/
```
* **Metadata** : 데이터를 설명해주는 데이터를 의미한다. <br>
  예를 들자면, 나는 반추동물에 있는 반추위액을 통하여 16S rRNA Seq 분석을 돌리기때문에 분석을 돌릴 Sample data를 설명해주는 데이터 이다. <br>
<br>

* Metadata  제작 포멧
  ![image](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/509d3e23-72c1-4a78-b06f-e64620a9ed9a) <br>
* Metadata는 Phynotype 형식으로 제작할수 있습니다. <br>
 phenotype 파일은 엑셀에서 아래와 같은 규칙으로 엑셀에서 작업하여, 다른이름으로저장-탭으로 분리된 텍스트 (.txt) 파일로 저장하여 이용가능하다. <br>
```
* 행의 규칙
- 1행: header (변수명으로 사용되며 대소문자 구분하여 사용)
- 2행: 변수의 type - categorical 또는 numeric 정보를 모든 변수에 대하여 빠짐없이 채운다.
- 3행 부터 샘플 나열
* 열의 규칙
- 1열 (필수) : header 에 ID 는 반드시 규정 에 맞게 표현
- 2열 (옵션): BarcodeSequence
- 3열 (옵션): LinkerPrimerSequence
- 2열 또는 4열부터 Phenotype 나열 : age, sex, bmi 등
결측값 : 공란만 허용 (NA, N/A, -99 등은 사용 불가) 
.txt 이든 .tsv 이든 사용에는 무관함. 실습파일의 형식에 맞추어 다음 분석에 같은 형식으로 만들면 실수 최소화 할수있다.

* QIIME2 에서 설명하는 Metadata 관련 링크 :
  https://gregcaporaso.github.io/q2book/using/metadata.html
  ```
* 해결책으로 교수님께서 전에 KOGO 학회에서 받은 Metadata에 실험할 Sample 정보만 바꿔서 확장자명 맞춘뒤 분석 진행 해보라고 조언을 해 주셨다..

**그래서 방향잡고 진행**
<br>
* Metadata 스크립트 내용 변경 -> 실험실에서 분석할 Sample로 기존 Sample ID를 변경하였다.
![image](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/675a82a7-f786-4d23-a3e8-22ca8fcc6dcd)

<br>

**그랬더니,,**
<br>

- overview
![image](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/a8d26d93-ffc6-451c-a8d8-2309f29d5b5d) <br>
- Interactive Sample Detail
![image](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/c3798e91-853c-43eb-bc8b-94ad6122892f) <br>
- Feature Detail
![image](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/4db2a7b9-e03a-47c5-9240-84493bafcf00) <br>
<br>

* https://view.qiime2.org/visualization/?type=html&src=b2c64c21-082e-4b38-b1d4-86a83cb8adf6 - 위 분석 결과 파일 Drag and Drop 파일 링크 <br>

* **문제점** <br>
  분석을 진행한 Metadata 파일이 온전히 분석하려는 Sample의 정보가 아니기때문에 Feature Table에대한 정보가 정확하지않다.

**그래서** Metadata를 우리가 분석하는 Ruminant 에 대한 내용으로 채우기 위해 기존에 선행 연구된 논문을 검색해서 Metadata에 대한 Format을 찾아서 밴치마킹 하기로 결정 <br>
하지만, 논문에 어떻게 Metadata를 작성했는지 제공을 해주지 않아서, 있는자료로 메타데이터 자체 제작. <br>

![image](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/f03ee72e-7dc1-461b-b110-4a92de26e823) <br>

제작된 데이터로 분석 시작.

**하지만...**

오류가 계속 뜬다......
![image](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/abf9d39b-d3a5-43e5-90ac-7dfcc650e815) <br>

그래서 Metadata 없이 그냥 Visualization 진행. <br>

* Overview <br>
![image](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/bfc06e83-22bb-4fcb-a7b3-0994a248e561) <br>

* Interactive Sample Detail <br>
![image](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/6b880b1a-8d2d-4166-9e94-a38cf8bd058b) <br>

* Feature Detail <br>
![image](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/c9a46682-fdca-4f27-8fb6-9de80dd6527c) <br>

이렇게 결과가 확인되었다.

* Qiime2 view 결과 확인 링크 <br>
  https://view.qiime2.org/visualization/?type=html&src=30ca39ab-af3c-4357-95c2-e1175219dd30 <br>

* **일단 Metadata가 없이도 분석이 가능하다는것을 확인** 그래서 다음 분석단계로 넘어감. <br>

**Metadata 관련 문제 해결! - .tsv 파일내에 샘플별데이터 정렬이 Tab으로 구분지어져 있어야했는데 그렇지 않고 하나로 묶여있었다... <br>
이점 해결하고 나니 분석이 진행 되었음!** <br>
![image](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/c0e3caaa-6bc4-4d01-a620-e108ed39d93c) <br>

*Overview <br>
![image](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/39fdea69-ac0d-408b-8a1b-a87aae9d8c16) <br>


* Interactive Sample Detail <br>
![image](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/8b3f7e3d-e07f-4149-853d-3dcf373ff78f) <br>

* Feature Detail <br>
![image](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/5e77581c-9495-4b73-b6f0-c8133edd135a) <br>


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

### 3-3-3. Data filtering 

```
qiime feature-table filter-samples \
--i-table table-dada2.qza \
--p-min-frequency 1 \
--o-filtered-table filtered_1_table.qza
```

**Data Filtering 단계는 Sample에서 나온 현저히 낮은 Feature들만 필터링을 진행한다고 했지만, 여기서는 어떤 Sample에서 우리가 확인하고싶은 미생물이 나올지 몰라 Feature 가 낮은 Sample도 살려서 다음단계로 넘어갔습니다.** <br>

**하지만,,,** Filter된 결과 파일이 다양성분석에서 Input 파일로 사용되기 떄문에 Filtering 단계를 진행 하였습니다. 
0으로 Filtering 진행 하려 하였으나, Qiime tool 내에서 필터링을 하지않는것은 요구되지 않는다는 오류코드를 보내와서 어쩔수 없이 샘플당 feature가 1개 나오는 샘플들을 Filtering  하였습니다. <br>

![image](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/9ab43df7-23c4-446a-91a2-cf2af03cd93d) <br>

* 결과 파일
  * filtered_1_table.qza
 
### 3-3-4. Visualize with Filtered Data


table-dada2.qza 파일에서 나타내었던 샘플당 Feature들을 filtering 하면서 filtered_1_table.qza 파일로 넘어오게 되는데 여기서 생기는 변화들을 filtered_1_table.qzv에서 확인할수 있다. <br>

![image](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/9fab6992-436f-4ed6-ae4f-db1ca3596f71)


```
qiime feature-table summarize \
--i-table filtered_1_table.qza \
--o-visualization filtered_1_table.qzv \
--m-sample-metadata-file sample-metadata_ata.tsv
```

* 결과 파일
  * filtered_1_table.qzv

* filtered_1_table.qzv 파일을 Drag and Drop으로 visualization 진행한 링크:
  https://view.qiime2.org/visualization/?type=html&src=2f97fb2d-f152-47ba-babe-d208c513a2c3 
    
## 4. Diversity Analysis <br>
Diversity Analysis Pipeline : <br>
![스크린샷 2024-03-13 21-33-02](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/b41ac96f-6c87-41c5-a857-bfea54d116e8) <br>

Diversity 분석은, QIIME2의 "diversity" 라는 plugin 을 사용하며, core-metrics-phylogenetic 방법으로, alpha 와 beta diversity metrics를 한번에 생성가능합니다. <br>

* Alpha diversity 

  * Shannon’s diversity index (a quantitative measure of community richness)
  * Observed Features (a qualitative measure of community richness)
  * Faith’s Phylogenetic Diversity (a qualitiative measure of community richness that incorporates phylogenetic relationships between the features)
  * Evenness (or Pielou’s Evenness; a measure of community evenness)
<br>

* Beta diversity

  * Jaccard distance (a qualitative measure of community dissimilarity)
  * Bray-Curtis distance (a quantitative measure of community dissimilarity)
  * unweighted UniFrac distance (a qualitative measure of community dissimilarity that incorporates phylogenetic relationships between the features)
  * weighted UniFrac distance (a quantitative measure of community dissimilarity that incorporates phylogenetic relationships between the features)
  * core-metrics-phylogenetic 방법에서는, FeatureTable[Frequency] 즉, 위에서 생성한 filtered_100_table.qza 파일을 user-specified depth 로 rarefying 합니다.

이를 위하여, filtered_100_table.qzv 을 QIIME2view 의 "Interactive Sample Detail"에서 확인한 후, 적절한 depth를 정합니다.

Rarefaction 은 이렇게 정한 기준 depth 로 replacement 없이 subsampling을 하며, 기준 depth 이하의 샘플은 분석에서 제외됩니다. 내 샘플 중 최소 read count를 기준으로 정한다면 분석에 제외되는 샘플은 없게 됩니다.

### 4-1. Phylogenetic Diversity 분석을 위한 Phylogenetic Tree 만들기 <br>


```
qiime phylogeny align-to-tree-mafft-fasttree \
--i-sequences rep-seqs.qza \
--o-alignment aligned-rep-seqs.qza \
--o-masked-alignment masked-aligned-rep-seqs.qza \
--o-tree unrooted-tree.qza \
--o-rooted-tree rooted-tree.qza
```

* 코드 실행 한 사진.
![image](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/26e215f6-ca8b-4873-b7c5-f5c7af2abb95)

* output 파일 1: aligned-rep-seqs.qza 생성 확인
* output 파일 2: masked-aligned-rep-seqs.qza 생성 확인
* output 파일 3: unrooted-tree.qza 생성 확인
* output 파일 4: rooted-tree.qza 생성 확인 => 이 rooted-tree.qza 파일이 phylogenetic diversity 분석에 사용됩니다.

### 4-2. Corer Analysis <br>

* 필요한 input 파일: filtered_100_table.qza, rooted-tree.qza, 메타데이터 sample-metadata_ata_s48.txt
* Tutorial 상에는 filtering 단계에서 사라진 샘플들을 Qiime2 view에 Visualization 시킨후 지워진 샘플들을 기존의sample-metadata_ata.tsv에서 지워서 파일명을 변경하였다. 그래서 sample-metadata_ata_s48.txt파일이 형성되었다. 
* 실제로는 지워진 샘플들이 없어서 제작한 sample-metadata_ata.tsv파일을 그대로 사용하여 분석을 진행하였다.

* --p-sampling-depth 명령어와 함께 해당 depth 숫자를 반드시 적습니다.

```
qiime diversity core-metrics-phylogenetic \
--i-phylogeny rooted-tree.qza \
--i-table filtered_1_table.qza \
--p-sampling-depth 2 \   # 2개의 Feature를 갖는샘플부터 다시 sampling을 진행한다는 코드
--m-metadata-file sample-metadata_ata.tsv \
--output-dir core-metrics-results
```

output 폴더: core-metrics-results 폴더 생성 확인

* 코드 진행한 사진
  ![image](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/783d4fcd-f7c6-4db5-9115-7c20527f3ff5) <br>

* Output 폴더에 들어가서 결과물 확인한 사진
  ![image](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/9dd16ed7-8605-4837-bbb9-7cb7fa15224a) <br>

* 분석을 진행하는 폴더에 Output 폴더가 생성된것을 확인할수 있다.
  ![image](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/82ae0999-0533-46d8-a610-bc91cb04dc56)

### 4-3. Beta Diversity 그룹간 비교 

* Unweighted UniFrac distance (phylogenetic binary 분석)

```
qiime diversity beta-group-significance \
--i-distance-matrix core-metrics-results/unweighted_unifrac_distance_matrix.qza \
--m-metadata-file sample-metadata_ata.tsv \
--m-metadata-column Description \
--o-visualization core-metrics-results/unweighted-unifrac-vegetation-significance.qzv \
--p-pairwise
```

* 코드 실행한 사진:
  ![image](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/fef34847-1eb6-445a-b3a7-d518b4cbc893) <br>
* Output 파일 Visualization 한 사진 :
  ![image](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/acae2520-f8b4-4f1c-a431-612b89f6f443) <br>
<br>

* alpha diversity 분석과는 달리, beta diversity 그룹 비교 분석은, 1개의 변수만 분석됩니다. --m-metadata-column 에서 분석변수 header name 을 반드시 지정해주어야 합니다.
* output 파일: core-metrics-results 폴더 안에 unweighted-unifrac-vegetation-significance.qzv 생성 확인
* 결과 보기
  * Overview : PERMAVONA 통계량 확인
  * Group significance plots : Distance to 기준그룹
  * Pairwise permanova results : 세그룹 이상 시, pairwise 통계분석결과
  * 모든 plots 은 PDF 다운 가능하며, TSV나 CSV 다운로드하여 직접 plot을 새로 그릴 수도 있음
<br>

* Weighted UniFrac distance (phylogenetic abundance 분석)

```
qiime diversity beta-group-significance \
--i-distance-matrix core-metrics-results/weighted_unifrac_distance_matrix.qza \
--m-metadata-file sample-metadata_ata_s48.txt \
--m-metadata-column Vegetation \
--o-visualization core-metrics-results/weighted-unifrac-vegetation-significance.qzv \
--p-pairwise
```
* 필요한 input 파일: core-metrics-results 폴더 안에 weighted_unifrac_distance_matrix.qza, 메타데이터 sample-meteadata_ata.tsv
* output 파일: core-metrics-results 폴더 안에 weighted-unifrac-vegetation-significance.qzv 생성 확인
* Output 파일 Visualization 한 사진 :
  ![image](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/ae49e811-f091-48fa-9a5c-1476fa88bac1)


## 5. Taxonomy Profiling 

Taxonomy Profiling Pipeline : <br>
![스크린샷 2024-03-13 21-37-06](https://github.com/Ju-M99/rumen_16s_rRNA_seq_profiling/assets/145320727/ea6c2704-7ab8-4558-ba16-5f9860f532e6) <br>

### 5-1. Classification

Taxonomic 분석을 위해서는, 기존 만들어놓은 feature table (filtered_1_table.qza)과 representative sequence (rep-seqs.qza) 파일 외에, taxonomy (features 의 이름) 정보가 필요합니다.

그러므로 taxonomic 분석 전에, rep-seqs.qza 파일에 Machine Learning 방법으로 train된 reference DB (QIIME2 홈페이지에서 다운로드 가능)의 taxonomy 정보를 붙이는 작업을 아래와 같이 진행합니다.

* Greengene DB 를 이용한 trained data : gg-13-8-99-nb-classifier.qza <br>

* 필요한 input 파일: gg-13-8-99-nb-classifier.qza, rep-seqs.qza
```
qiime feature-classifier classify-sklearn \
--i-classifier gg-13-8-99-nb-classifier.qza \
--i-reads rep-seqs.qza \
--o-classification greengene138_99_taxonomy.qza
```

* output 파일: greengene138_99_taxonomy.qza 생성 확인

* 나의 representative sequences 데이터에 taxonomy 가 붙은 것을 확인하기 위해, 위 생성된 .qza 파일을 Visualization

```
qiime metadata tabulate \
--m-input-file greengene138_99_taxonomy.qza \
--o-visualization greengene138_99_taxonomy.qzv
```

* output 파일: greengene138_99_taxonomy.qzv 생성 확인

* 코드 실행 한 사진:
  ![image](https://github.com/yoonseok95/rumen_16s_rRNA_seq_profiling/assets/145320727/0051996e-a921-4266-94b5-f60cc7bf4659)
 
* 파일을 Drag and Drop으로 visualization 진행한 사진:
  ![image](https://github.com/yoonseok95/rumen_16s_rRNA_seq_profiling/assets/145320727/59fa2356-32b4-490a-936c-1608c2a2c265)

* 파일을 Drag and Drop으로 visualization 진행한 링크:
  https://view.qiime2.org/visualization/?type=html&src=c35c5941-152d-450c-b205-9548235d35e3

### 5-2. Taxonomic Composition에 대해 Bar plot 그리기

```
qiime taxa barplot \
--i-table filtered_1_table.qza \
--i-taxonomy greengene138_99_taxonomy.qza \
--m-metadata-file sample-metadata_ata.tsv \
--o-visualization taxa-bar-plots_greengene.qzv
```

* output 파일: taxa-bar-plots_greengene.qzv 생성 확인

* 코드 실행한 사진 :
  ![image](https://github.com/yoonseok95/rumen_16s_rRNA_seq_profiling/assets/145320727/0d32d7d9-0c09-4def-a255-dac2ec1bbbb9)

* Output 파일 Visualization  사진:
  ![image](https://github.com/yoonseok95/rumen_16s_rRNA_seq_profiling/assets/145320727/d3aaba04-7e22-4301-8f85-dbe64da5201a)
* Taxa bar plot visualization 한 Qiime2 view 링크 : <br>
  https://view.qiime2.org/visualization/?src=ae8e5616-64c0-4cca-bc3f-51a8e3a05ba4&type=html
<br>

**문제점** <br>

위의 Output 파일 Visualization 사진에서도 보이는 바와 같이 우리가 중점으로 보고싶은 미생물들에 대한 정보에 비해 박테리아와 같은 우리가 Target 하지 않은 미생물들에 대한 정보들이 더 많이 있다. 
하여, 2023년 12월15일자로 제작된 한경국립대학교 반추동물 저메탄 성능 검증 최종보고서에 실려있는 소 반추위 내 Methanogen 종류 (P.g 25, **표 13. 소의 반추위 내 Methanogen 종류**) 를 참고하여 Silva Data Base 에서 Methanogen 에 대한 Reference Data들을 다운받아 분석을 진행하고자 함.
