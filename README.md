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
<br>

# 프로젝트 내용

>MMSegmentation을 활용하여 전체적인 프로젝트를 수행

<br>

***
## EDA

<img width="821" alt="스크린샷 2022-06-08 21 50 38" src="https://user-images.githubusercontent.com/96764429/172620713-5aa53791-b2cc-4af9-a724-41bf52ac2c1c.png">

<br>

<img width="933" alt="스크린샷 2022-06-08 21 52 33" src="https://user-images.githubusercontent.com/96764429/172621068-52e1933f-9a45-4cb3-8989-b96636828e18.png">

<pre><code>{'geometry': {'coordinates': [[[31.4347031225, 30.0413951468, 0.0],
      [31.4405428056, 30.0414645232, 0.0],
      [31.4404632046, 30.0465452603, 0.0],
      [31.4346232236, 30.0464758698, 0.0]]],
    'type': 'Polygon'},
   'properties': {'building_imcoords': '821.5515067078223,969.1356097092277,799.4138912576116,1009.1063042721082,798.7989574951057,1020.4825788784664,816.3245697265226,1024,847.6861916143212,997.7300296657498,847.0712578518154,986.9686888218974',
    'image_id': 'BLD00001_PS3_K3A_NIA0276.png',
    'ingest_time': '2020-10-27T02:04:23.355595Z',
    'object_imcoords': 'EMPTY',
    'road_imcoords': 'EMPTY',
    'type_id': '2',
    'type_name': '아파트'},
   'type': 'Feature'}
</pre></code>

jeojson 파일은 위와 같이 구성

<br>

<img width="847" alt="스크린샷 2022-06-08 21 55 34" src="https://user-images.githubusercontent.com/96764429/172621738-50eab779-f30b-4f0a-9442-4077bc519ffe.png">


<br>

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
## LV1. 건물, 도로 각각 검출   

## Ablation Study
**Loss function**이 모델의 성능에 미치는 영향을 파악하고자 Ablation Study 진행  

<pre><code>Crop size: 512 x 512  
Augmentation: default  
iteration: 20k
</pre></code>

<br>

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
| Dice, Focal, Lovasz |	87.49	| **83.35** |
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

<br>

**Road** *default* Augmentation  
<pre><code>random resize with ratio 0.5 ~ 1.5  
random cropping to 512 x 512
random horizontal flipping prop 0.5  
PhotometricDistortion
</pre></code>

<br>

* Road의 경우 Building 보다 Class imbalance가 더욱 심함
* Class imbalance를 잡아주기 위한 Loss function인 **Focal Loss**와 **OHEM Sampler**의 성능을 비교

<br>

| Loss function |	Augmentation | Sampler |	mIoU |	Road IoU |
| --- | --- | --- | :---: | :---: |
| Dice, Lovasz	| default |  |	78.89 |	65.76 |
| Dice,Lovasz |	default	| OHEM | 79.08	| 66.03 |
| Dice, **Focal**, Lovasz |	default |	 | 79.22	| **66.32** |

OHEM Sampler를 사용하는 것보다 Focal Loss를 사용하는 것이 보다 모델의 성능이 높게 나오는 것을 확인  

<br>

* 성능 향상을 위해 Road Model에 **CutOut** augmentation을 적용

<br>

| Loss function | Augmentation | mIoU | Road IoU | ➡️ | Augmentation | mIoU | Road IoU |
| --- | --- | :---: | :---: | --- | --- | :---: | :---: |
| CrossEntropy, Lovasz	| Default	| 79.17 |	66.12	| ➡️ |	CutOut | 79.09 |	**66.61** |
| Focal, Lovasz	| Default |	79.24 |	66.39	| ➡️	| CutOut	| 79.17 |	**66.42** |
| CrossEntropy, Focal, Lovasz |	Default	| 79.12	| 66.03	| ➡️ |	CutOut |	79.1	| **66.18** |
| Dice, Focal, Lovasz	| Default |	79.25 |	66.3	| ➡️	| CutOut	| 79.44	| **66.71** |
| CrossEntropy ,Dice, Focal, Lovasz |	Default	| 79.22 |	66.32	| ➡️ |	CutOut	| 79.25 |	**66.4** |

**CutOut**을 적용했을 때 성능 향상됨을 확인   

<br>

### Road Inference 결과

<img width="1129" alt="Road Inference Result" src="https://user-images.githubusercontent.com/96764429/172583294-7f768c60-7fd5-4e89-ac09-e2521fb7b4bc.png">

* 좌측의 이미지와 같이 대체로 길을 잘 잡아냄
* 중간 이미지의 동그란 길은 라벨링 되어 있지 않은 길이지만 잡아냄을 확인
* 우측 이미지와 같이 건물 사이의 골목길처럼 육안으로 확인했을 때 알아보기 어려운 길을 잘 잡아내지 못하는 한계

<br>

### Building Inference 결과

<img width="821" alt="LV1 Building Inference Result" src="https://user-images.githubusercontent.com/96764429/172602973-d3db3592-3dc6-4898-8866-56cbc3816742.png">

* 좌측의 이미지와 같이 건물을 잘 검출해냄
* 하지만 우측의 이미지에서와 같이 두 개 이상의 건물을 한 덩어리로 잡아내는 한계
* 이러한 한계점을 극복하기 위해서 LV2 진행

<br>
<br>

## LV2. 건물 객체 검출

<img width="421" alt="image" src="https://user-images.githubusercontent.com/96764429/172608620-aaeb88e9-3e56-411c-ab22-464fa5c13f32.png">

* 위의 이미지와 같이 건물의 Boundary에 Contour 처리
* LV1과 달리 Background, Building, Boundary 3개의 class로 학습을 진행

<br>

LV1에서 수행한 Ablation Study에서 결과가 잘 나온 Loss Function의 조합을 이용하여 모델 학습을 진행

| Loss function |	mIoU	Building | IoU |
| --- | :---: | :---: |
| CrossEntropy, Focal, Lovasz	| 74.55	| 79.27 |
| Dice, Focal, Lovasz	| 74.93	| **79.42** |

<br>

* 위의 결과를 토대로 이후의 실험에서는 **Dice**, **Focal**, **Lovasz**의 Loss Function 조합을 사용
* 위의 결과보다 좋은 성능을 이끌어내기 위해서 Hard Augmentation인 **CutOut** 적용

CutOut의 최적의 하이퍼파라미터를 찾기 위한 실험결과(max_iter=20k)
|	Augmentation |	mIoU |	Building IoU |
| --- | :---: | :---: |
| Random CutOut	| 74.92	| 79.2 |
| Random CutOut	| 74.3	| 78.99 |
| Random CutOut	| 73.56	| 78.81 |
| Random CutOut	| 74.19	| 78.82 |
| Random CutOut	| 74.8	| 79.53 |
| Random CutOut	| 74.76	| 79.32 |
| Random CutOut	| 75.02	| 79.62 |
| Random CutOut	| 75.22	| 79.7 |
| Random CutOut	| 74.9	| 79.61 |
| Random CutOut	| 74.82	| 79.31 |
| Random CutOut	| 74.75	| 79.22 |

* <code>RandomCutOut(prob=0.5, n_holes=(1,100), cutout_ratio=[(0.25,0.75)]</code>일 때 좋은 결과가 나옴을 확인
* 이를 토대로 batch size=2, max_iter=50k 모델 학습 수행시 아래와 같은 결과

|	Augmentation |	mIoU |	Building IoU |
| --- | :---: | :---: |
| Random CutOut	| 75.4	| **80**	|

<br>

### LV2 Building Inference 결과

<img width="868" alt="LV2 Building Inference Result" src="https://user-images.githubusercontent.com/96764429/172614485-beede17f-8366-4da4-88ee-16723bd52b7c.png">

* 좌측 이미지와 중간 이미지를 보면 대체로 건물을 객체별로 잘 분리해 냄을 확인
* 우측 이미지와 같이 소형 건물이 밀집해 있는 지역도 어느 정도 분리하지만 보완이 필요

<br>

## LV1, LV2 Inference 결과 

<img width="591" alt="LV1, LV2 Inference 비교 2" src="https://user-images.githubusercontent.com/96764429/172615690-0ced4a6a-fae0-4ef3-9b8e-d8bdd26ebb23.png">

<br>

<img width="788" alt="LV1, LV2 Inference 비교" src="https://user-images.githubusercontent.com/96764429/172615365-adbdd4a8-ae19-4006-94a1-5e15cb63d388.png">

<br>

## LV3. 폴리곤 지도 매핑

<img width="947" alt="Inference result -  contour" src="https://user-images.githubusercontent.com/96764429/172617873-7111cf47-5c3d-408a-93ba-ffd2bc69e2f3.png">

<br>

<img width="600" alt="image" src="https://user-images.githubusercontent.com/96764429/172618327-0ddcde66-552a-41cb-b275-72f5b08c03a4.png">

<br>

### LV3 폴리곤 매핑 결과

<img width="600" alt="image" src="https://user-images.githubusercontent.com/96764429/172618823-32d81f87-e4d0-4b99-811e-1f92d3158fa8.png">

<br>

<img width="600" alt="image" src="https://user-images.githubusercontent.com/96764429/172619028-3d9824da-faa0-4575-80b3-15aaee2a65c7.png">

<br>

<img width="600" alt="image" src="https://user-images.githubusercontent.com/96764429/172619063-2d1338ce-903b-4421-9665-48c8796ea4c8.png">

<br>
