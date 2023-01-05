# Sketch2Fashion
손그림 의류 추천 시스템




## Introduction

본 프로젝트는 사람이 손으로 그린 의류 스케치를 실제 의류 이미지로 변환하고 변환된 이미지로 실제 쇼핑몰에서 판매하는 상품을 검색하는 서비스를 제공한다.

## ✨ Demo

### modify
<p align ="center">
  <img src = "https://user-images.githubusercontent.com/90328527/210715156-50f9fc38-2b47-4b58-b7ba-18eb62bfcf26.gif">
</p>

<p align ="center">
  <img src = "https://user-images.githubusercontent.com/90328527/210715208-c9645dee-884d-4702-9acf-517b9010f1d9.gif">
</p>

<p align ="center">
  <img src = "https://user-images.githubusercontent.com/90328527/210715257-4de5b579-5c74-4b24-a538-6ad24c1f2d14.gif">
</p>


### colorization
<p align ="center">
  <img src = "https://user-images.githubusercontent.com/90328527/210715306-cec0fda6-60c2-47bf-8521-742aabdffb60.gif">
</p>

<p align ="center">
  <img src = "https://user-images.githubusercontent.com/90328527/210715355-b3731542-17ed-4f9c-a76e-4457cae80051.gif">
</p>


### visual search
<p align ="center">
  <img src = "https://user-images.githubusercontent.com/90328527/210715389-980350ef-42e9-423c-b7d3-4ee5f7e64148.gif">
</p>

## Dataset

|Data|데이터 수|Train 데이터 수|Val 데이터 수|세부사항|
|:-:|:-:|:-:|:-:|:-:|
|1|2543|1889|654|hat|
|2|2589|1912|677|pants|
|3|2549|1892|657|t-shirts|
|4|2537|18188689|651|skirt|


학습에는 fashion-outfit-items 데이텃 셋을 활용, 카테고리 별로 약 2500개로 구성된다.

출처 : https://www.kaggle.com/datasets/kritanjalijain/fashionoutfititems

## Model

![project_pipeline](https://github.com/SangBeom-Hahn/Sketch2Fashion/blob/main/assests/model.png)


전체적인 파이프라인은 2 stage로 이루어져있다. 1단계에서도 2개로 나뉜다. A는 고객이 그린 의류 sketch를 채색 모델을 통해 채색을 하는 것이고 B는 고객이 그린 의류 sketch를 실제 의류 이미지로 변환하는 것이다. A는 sketch에 고객이 원하는 색으로 점을 찍거나 선을 그리는 등 단순한 처리로 완벽한 채색 결과를 생성해내고 검은 색 선으로 스케치의 영역을 구분하는 등 커스터마이징을 할 수 있다. 

2단계에서는 1단계에서 나온 결과물을 MS visual search API의 입력으로 넣어 실제로 입력 이미지와 유사한 제품을 판매하고 있는 쇼핑몰의 URL을 반환한다.


<!--
## Project Structure

```
OpenSW_Team5
├── Final Project_MMDetection
├── mmdetection_code
├── team_assignment
└── bot.py
```

- Final Project_MMDetection : 데이터 전처리
- mmdetection_code : MASK-RCNN 코드
- bot.py : 텔레그램 봇 실행 코드

-->


<!--

## Local
```
python==3.7.13
cuda 10.0 - rtx 2080 super
```
--> 



## Requirements
```
tensorflow==2.x
tensorflow-GPU==2.x
```

## reference
- [Sketch2Fashion: Generating clothing visualization from sketches](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/24693891-8915-4e8b-94b9-5a98831188f0/55752208.pdf?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20221220%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20221220T093913Z&X-Amz-Expires=86400&X-Amz-Signature=2822a6743f941bcbc812850571d23c7ac23cd3c2d4f08c3e383aa91a7dd60fe2&X-Amz-SignedHeaders=host&response-content-disposition=filename%3D%2255752208.pdf%22&x-id=GetObject)
- [Generative Visual Manipulation on the Natural Image Manifold](https://arxiv.org/abs/1609.03552)
- [Pix2pix-edges-with-color](https://github.com/michaelnation26/pix2pix-edges-with-color)
- [Sketch Your Own GAN](https://arxiv.org/abs/2108.02774)
- [DeepFaceDrawing: Deep Generation of Face Images from Sketches](http://geometrylearning.com/paper/DeepFaceDrawing-supple.pdf)

<!--
## Authors

|ㄹㄴ|한상범|홍찬의|
|:-:|:-:|:-:|
|[Github](https://github.com/SunWoo98Pi)|[Github](https://github.com/SangBeom-Hahn)|[Github](https://github.com/hcu55)|

-->
