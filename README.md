# 클라우드컴퓨팅 프로젝트 (Introduce and Using Amazon Sagemaker)

## 프로젝트 멤버 이름 및 담당 파트
- 김동영: SageMaker 를 테스트하기 위한 샘플코드를 선정하여 테스트해보는 역할을 수행하였습니다. Amazon
SageMaker 는 인공지능을 코딩하고 배포할 수 있는 환경이 구성되어 있는데, 이 환경 중 일부를 테스트해보았습니다. 
첫번째로, 기계학습 코드 1개를 이용하여, 다양한 유형의 노트북 인스턴스 실행시간을 비고하였습니다.
두번째로, Tensorflow와 Pytorch 샘플코드를 테스트 하였습니다. 
마지막으로, 마켓플레이스에 있는 알고리즘을 이용하여 모델을 추출하는 테스트를 수행하였습니다.

- 우건희: Amazon SageMaker의 기능들을 조사/소개하는 역할을 수행하였습니다. 
현재 Amazon SageMaker 개발자 안내서와 국내외 인터넷 자료들을 참고하여 조사를 완료하였습니다. 
특히나, SageMaker, Autopilot, GroundTruth, Built-in Algorithms, Amazon Augmented AI 등을 중점적으로 조사하였습니다. 

## 프로젝트 소개 및 개발 내용 소개

Amazon SageMaker는 가장 포괄적인 ML/DL 서비스입니다. 데이터처리/개발/훈련/배포를 위한 통합적인 기능을 제공하며, IDE인 Amazon SageMaker를 제공하고 있습니다. SageMaker는 Jupyter Notebook, Tensorflow, Pytorch 등. ML/DL개발에 필요한 라이브러리와 환경을 제공합니다. 주요기능으로는 데이터 수집도구인 Amazon SageMaker Data Wrangler, Feature를 저장/관리하는 관리형 서비스인 Amazon SageMaker Feature Store, 통합 개발 도구인 Amazon SageMaker Studio, Jupyter Notebook / Jupyter Lab 기능을 제공하는 노트북 인스턴스, 알고리즘, 모델, 데이터셋을 구독할 수 있는 Marketplace등 다양한 기능이 있습니다.

저희는 Amazon Sagemaker를 소개하고, 이 도구를 이용해 몇가지 테스트를 진행하였습니다.
진행한 테스트는 다음과 같습니다:
- 다양한 노트북 인스턴스에서의 실행시간 비교
- 다양한 라이브러리 샘플코드를 실행
- 마켓플레이스 알고리즘을 이용한 모델 훈련

## 테스트에 사용된 코드 소개

- [Logistic Regression](https://github.com/op2gs2/CloudComputing_Project/blob/main/Logistic%20Regression_Sample.ipynb): Logistic Regression을 수행하는 머신러닝코드입니다. 여러 유형의 노트북 인스턴스의 실행시간을 측정하기 위해 쓰인 코드입니다.

- [Tensorflow SampleCode](https://github.com/op2gs2/CloudComputing_Project/blob/main/classification_Tensorflow_sample.ipynb): 이미지 분류를 수행하는 Tensorflow 샘플코드입니다. 노트북 인스턴스 환경에서 Tensorflow의 구동여부를 확인하기 위해 쓰인 코드입니다. [Tensorflow 공식홈페이지](https://www.tensorflow.org/tutorials/keras/classification?hl=ko)에서 가져왔습니다.

- [Pytorch SampleCode](https://github.com/op2gs2/CloudComputing_Project/blob/main/optimization_tutorial_Pytorch_sample.ipynb): 구한 모델을 최적화하는 Pytorch 샘플코드입니다. 노트북 인스턴스 환경에서 Pytorch의 구동여부를 확인하기 위해 쓰인 코드입니다. [Pytorch 공식홈페이지](https://tutorials.pytorch.kr/beginner/basics/optimization_tutorial.html)에서 가져왔습니다.

- 마켓플레이스 알고리즘과 데이터셋
  - [알고리즘](https://aws.amazon.com/marketplace/pp/prodview-vcfitb65ln2ro?sr=0-1&ref_=beagle&applicationId=AWS-Marketplace-Console): 사기 거래인 확률을 계산하는 Autoencorder 알고리즘입니다. 불균형이 심한 데이터셋에서도 사기 거래를 탐지할 수 있다고 합니다.
  - [데이터셋](https://www.kaggle.com/mlg-ulb/creditcardfraud): 2013년 9월 유럽 내 카드 거래 내역을 기반으로 한 데이터셋입니다. 본 데이터셋은 전체 284,807건의 거래 중, 492건의 사기 거래 데이터를 가지고 있습니다. 이는 불균형데이터에 해당하는 데이터셋입니다.

## 테스트 결과 소개

### 다양한 노트북 인스턴스에서의 실행시간 비교

|인스턴스 유형|인스턴스 이름|vCPU/CPU|메모리(GiB)|네트워크대역폭|실행시간(초)|
|---|---|---|---|----|---|
|범용|ml.t2.medium|2|4|낮음에서 중간|1525.2446|
|컴퓨팅 최적화|ml.c5.xlarge|4|8|최대 10|416.2102|
|메모리 최적화|ml.r5.large|2|16|최대 10|559.9665|

### 다양한 라이브러리 샘플코드를 실행

- Tensorflow 실행 결과

![Tensorflow 실행 결과](https://github.com/op2gs2/CloudComputing_Project/blob/main/img/%EB%9D%BC%EC%9D%B4%EB%B8%8C%EB%9F%AC%EB%A6%AC%20%ED%85%90%EC%84%9C%ED%94%8C%EB%A1%9C%EC%9A%B0%20%EC%8B%A4%ED%96%89%EA%B2%B0%EA%B3%BC_%EB%85%B8%ED%8A%B8%EB%B6%81%20%EC%8B%A4%ED%97%98.jpg?raw=true)

<br>

- Pytorch 실행 결과

![Pytorch 실행 결과](https://github.com/op2gs2/CloudComputing_Project/blob/main/img/%EB%9D%BC%EC%9D%B4%EB%B8%8C%EB%9F%AC%EB%A6%AC%20%ED%8C%8C%EC%9D%B4%ED%86%A0%EC%B9%98%20%EC%8B%A4%ED%96%89%EA%B2%B0%EA%B3%BC_%EB%85%B8%ED%8A%B8%EB%B6%81%20%EC%8B%A4%ED%97%98.jpg?raw=true)

### 마켓플레이스 알고리즘을 이용한 모델 훈련
- 훈련 작업 세부사항 페이지

![훈련 작업 세부사항 페이지](https://github.com/op2gs2/CloudComputing_Project/blob/main/img/%ED%9B%88%EB%A0%A8%EC%9E%91%EC%97%85%EC%99%84%EB%A3%8C%EC%84%B8%EB%B6%80%EC%82%AC%ED%95%AD_%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98%20%EC%8B%A4%ED%97%98.jpg?raw=true)

- 실행 Log

![실행 Log](https://github.com/op2gs2/CloudComputing_Project/blob/main/img/%ED%9B%88%EB%A0%A8%EC%83%81%ED%83%9C%EA%B8%B0%EB%A1%9D_%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98%20%EC%8B%A4%ED%97%98.jpg?raw=true)

- 실행결과 및 출력파일([autoencoder-model.h5](https://github.com/op2gs2/CloudComputing_Project/blob/main/src/autoencoder-model.h5?raw=true))

![실행결과 및 출력파일](https://github.com/op2gs2/CloudComputing_Project/blob/main/img/h5%ED%8C%8C%EC%9D%BC%EB%82%B4%EC%9A%A9_%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98%20%EC%8B%A4%ED%97%98.jpg?raw=true)

## 개발 결과물의 필요성 및 활용 방안

저희는 본 서비스를 다른 사람에게 소개하고, 샘플 소스코드를 가져와서 직접 구동하며 시연하는
프로젝트를 진행하였습니다. 본 프로젝트는 AWS SageMaker 상에서 개발하고, 가상머신을
구동하는, 다양한 기능을 소개하는데 그 목적이 있습니다. AWS SageMaker 에는 ML 개발에 필요한
다양한 도구들이 있습니다. 따라서 이 도구들을 사용하게끔 유도하여, 다른 이들이 더 효율적인
코딩/개발을 할 수 있도록 도움이 될 것입니다. 다른 학우들에게, 지금 배웠던 내용과는 다른, 또 다른
서비스를 소개합니다. 이를 통해, 클라우드에 대한 이해도가 증가할 수 있을 것입니다.
최근 들어, 머신러닝과 같은 인공지능은 다양한 분야에서 사용되고 있습니다. 본 도구는 인공지능을
개발하는 도구이므로, 인공지능 개발과 관련한 다양한 분야에서 쓰일 수 있을 것입니다. 
