# CHEOLLIAN

## Table of Contents
* [🗓Milestone](#-milestone20220420--20220610)
* [🌏CHEOLLIAN](#-cheollian)
* [🧑‍💻Project](#-project)
* [💿Dataset](#-dataset)
* [Base Model](#base-model)
* [Ablation Study](#ablation-study)

<br>

***
## 🗓 Milestone(2022.04.20 ~ 2022.06.10)

| 단계 | 내용 | M1 | M2 | H1 | H2 | H3 | H4 | H5 | H6 |  
| --- |:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|---:|  
| 1 | 데이터셋 확인/전처리 | ☑️ | ◼️ | ◼️ | ◼️ | ◼️ | ◼️ | ◼️ | ◼️ |  
| 1 | 건물, 도로 검출 |  ☑️ | ☑️ | ◼️ | ◼️ | ◼️ | ◼️ | ◼️ | ◼️ |  
| 1 | LV1 결과물 분석 | ◼️ | ☑️ | ◼️ | ◼️ | ◼️ | ◼️ | ◼️ | ◼️ |   
| 2 | 건물의 객체 검출 | ◼️ | ◼️ | ☑️ | ☑️ | ◼️ | ◼️ | ◼️ | ◼️ |   
| 2 | LV2 결과물 분석 | ◼️ | ◼️ | ◼️ | ☑️ | ☑️ | ◼️ | ◼️ | ◼️ |   
| 3 | LV2 결과를 이용한 폴리곤 매핑 | ◼️ | ◼️ | ◼️ | ◼️ | ◼️ | ☑️ | ☑️ | ◼️ |  
| 3 | LV3 결과 분석 | ◼️ | ◼️ | ◼️ | ◼️ | ◼️ | ◼️ | ☑️ | ◼️ |  
| 4 | 발표 준비 | ◼️ | ◼️ | ◼️ | ◼️ | ◼️ | ◼️ | ◼️ | ☑️ |  

<br>

***
## 🌏 CHEOLLIAN

| 조원 | 담당 역할 | 역할 |
| --- |:---: | :---: |
| 박민규 | EDA | 데이터 전처리, 모델 구현, CV |
| 권민호 | 라이브러리 분석 및 구현 | 데이터 전처리, 모델 구현, CV |
| 김보성 | 건물 모델 | 데이터 전처리, 모델 구현, CV |
| 양우민 | 도로 모델 | 데이터 전처리, 모델 구현, CV |

#### co-operation Tool
| Tool | 용도 | Link |
| --- | :---: | :---: |
| Github | 코드 업로드 및 프로젝트 제출 | [🔗](https://github.com/CHEOLLIAN/Satellite-image-object-segmentation) |
| notion | 회의 내용 및 자료 정리 | [🔗](https://www.notion.so/SIA-0571b4a4e0be4bea909a9e9c05ff837b) |
| Slack | 멘토님 및 퍼실님과 소통 | 🔗 |
| Google Meet | 회의 및 소통 | 🔗 |
| Google Drive | 파일 공유 | 🔗 |
| Google Cloud |  | 🔗 |
| Figma | 회의 내용 및 자료 정리 | 🔗 |

<br>

***
## 🧑‍💻 Project

<br>

>👉프로젝트 요약  
본 프로젝트는 인공위성 영상에서 객체를 탐지 하기 위해 다양한 인공지능 기술을 시도한 
AIFFEL 해커톤 프로젝트  

<br>

### 주제: 위성영상 객체분할을 위한 의미론적 분할 기술

* Keyword: 의미론적 분할(Semantic Segmentation), Instance Segmentation

<br>

### 배경

* 의미론적 분할(Semantic Segmentation)은 위성으로부터 관찰되는 특정픽셀을 분류하는 방법으로써 전통적으로 많은 연구가 수행됨
* 인공지능 분석결과를 육안으로 분석해야하는 한계를 넘기 위해 Instance Segmentation 분석 수요 증가
* 객체의 ID가 구분되는 Instance Segmentation은 향후 고차원적인 분석방법을 지원

<br>

### 연구 목표

* 위성 영상에서 건물과 도로를 식별하고 객체를 분할한다.
 - 건물, 도로 각각 Semantic Segmentation

<br>

### 세부 목표

* 레벨별 스텝(순서대로 진행)

1. [LV1] 건물과 도로를 각각 검출하고 결과를 합쳐서 분석한다 (일반 ★☆☆☆☆)
2. [LV2] 건물의 객체검출을 위한 학습을 수행한다. (어려움 ★★☆☆☆)
3. [LV3] 건물의 크기와 개수를 계산할 수 있도록 LV2결과를 이용해 Polygon형태로
나타내고 지도에 매핑한다. (일반 ★★☆☆☆)

<br>

***
## 💿 Dataset

Dataset: 위성영상 객체판독 소개

| | 위성영상 객체판독 소개 |
|---|---|
| Link | [Link](https://aihub.or.kr/aidata/7982) |
| 데이터 분야 | 비전 |
| 구축기관 | 한국항공우주연구원 |
| 소개 | 아리랑 위성 영상을 활용한 학습 데이터셋 5종(관심객체 검출, 건물 윤곽 추출, 도로 윤곽 추출, 구름 추출, 레이더영상 수계 추출)</br> 구축하여 재난, 환경, 에너지, 자원, 안보, 식량 등 위성 영상을 다루는 다양한 분야에서 효율적으로 분석, 활용할 수 있도록 데이터 제공 |
| 주요 키워드 | 위성영상, 객체검출, 건물 윤곽 추출, 도로 윤곽 추출, 수계 검출, 구름 추출 |
| 구축 목적 | 아리랑 위성영상(광학 및 레이다 영상)을 이용한 다양한 위성정보 획득</br> 아리랑 위성 AI 데이터 구축·제공을 통해 국내 AI 위성 분석 서비스 산업 육성 |

<br>

***
## Base Model
### 모델 별 성능 비교

| Backbone |	Model | Crop_size |	Augmentation |	Loss function |	mIoU |	Building IoU |
| --- | --- | --- | --- | --- | :---: | :---: |
| ResNet101 |	Semantic FPN |	512x512 |	default	|CrossEntropy|	77.43	| 69.61|
| ResNet101 |	DeepLabV3 |	512x512 |	default |	CrossEntropy	| 85.4	| 80.52|
| ResNet101 | DeepLabV3+ |	512X512	|default |	CrossEntropy	| 86.03	| 81.34|
| HRNetV2 |	FCN |	512X512 |	default|	CrossEntropy |	78.52|	72.98 |
| **MiT-B5** |	**Segformer**|	512x512 |	default |	CrossEntropy |	**87.18** |	**82.88** |

<br>

**Building** *default* Augmentation  
<pre><code>random resize with ratio 0.5 ~ 2.0  
random cropping to 512 x 512
random horizontal flipping prop 0.5  
PhotometricDistortion
</pre></code>

<br>

<br>

## Ablation Study
**Loss function**이 모델의 성능에 미치는 영향을 파악하고자 Ablation Study 진행  

Crop size: 512 x 512  
Augmentation: default  
iteration: 20k

### Building
| Loss function |	mIoU |	Building IoU |
| --- | :---: | :---: |
| CrossEntropy |	87.18 |	82.88 |
| Dice	| 87.59	| **83.51** |
| Focal |	87.17|	82.88 |
| Lovasz	|87.19	| 82.97 |
| CrossEntropy, Dice	| 87.41	| 83.23 |
| CrossEntropy, Focal	| 87.22	| 82.92|
| CrossEntropy, Lovasz	| 87.45	| 83.28|
| Dice, Focal	| 87.33	| 83.19 |
| Dice, Lovasz	| 87.32	| 83.13 |
| Focal, Lovasz	| 87.32	| 83.12 |
| CrossEntropy, Dice, Focal	| 87.07	| 82.78 |
| CrossEntropy, Dice, Lovasz	| 87.43	| 83.31 |
| CrossEntropy, Focal, Lovasz	| 87.64	| **83.51** |
| Dice, Focal, Lovasz |	87.49	| 83.35 |
| CrossEntropy, Dice, Focal, Lovasz	| 87.42	| 83.23 |

<br>

### Road

| Loss function |	mIoU |	Road IoU |
| --- | :---: | :---: |
| CrossEntropy	| 78.45	| 64.77 |
| Dice	| 78.8	| 65.45 |
| Focal	| 78.38	| 64.62 |
| Lovasz	| 78.64	| 65.4 |
| CrossEntropy, Dice	| 78.58	| 64.99 |
| CrossEntropy, Focal	| 78.66	| 65.13 |
| CrossEntropy, Lovasz	| 79.17	| 66.12 |
| Dice, Focal	| 78.93	| 65.66 |
| Dice, Lovasz	| 78.89	| 65.76 |
| Focal, Lovasz	| 79.24	| **66.39** |
| CrossEntropy, Dice, Focal	| 78.68	| 65.16 |
| CrossEntropy,Dice, Lovasz	| 78.64	| 65.11 |
| CrossEntropy, Focal, Lovasz	| 79.12	| 66.03 |
| Dice, Focal, Lovasz	| 79.22	| **66.32** |
| CrossEntropy, Dice, Focal, Lovasz|	79.25 |	66.3 |

**Road** *default* Augmentation  
<pre><code>random resize with ratio 0.5 ~ 1.5  
random cropping to 512 x 512
random horizontal flipping prop 0.5  
PhotometricDistortion
</pre></code>

<br>

