# 클라우드컴퓨팅 프로젝트 (Introduce and Using Amazon Sagemaker)

## 프로젝트 멤버 이름 및 담당 파트
- 김동영: SageMaker 를 테스트하기 위한 샘플코드를 선정하여 테스트해보는 역할을 수행하였습니다. Amazon
SageMaker 는 인공지능을 코딩하고 배포할 수 있는 환경이 구성되어 있는데, 이 환경 중 일부를 테스트해보았습니다. 
첫번째로, 기계학습 코드 1개를 이용하여, 다양한 유형의 노트북 인스턴스 실행시간을 비고하였습니다.
두번째로, Tensorflow와 Pytorch 샘플코드를 테스트 하였습니다. 
마지막으로, 마켓플레이스에 있는 알고리즘을 이용하여 모델을 추출하는 테스트를 수행하였습니다.

- 우건희: 저는 Amazon SageMaker 의 모델의 소개, 기능들을 조사하는 역할을 수행하였습니다. 
현재 Amazon SageMaker 개발자 안내서와 국내외 인터넷 자료들을 참고하여 조사를 완료하였습니다. 
특히나, SageMaker, Autopilot, GroundTruth, Built-in Algorithms, Amazon Augmented AI 등을 중점적으로 조사하였습니다. 

## 프로젝트 소개 및 개발 내용 소개

<b> TODO: 작성 필요 </b>

## 테스트에 사용된 코드 소개

- [Logistic Regression](https://github.com/op2gs2/CloudComputing_Project/blob/main/Logistic%20Regression_Sample.ipynb): Logistic Regression을 수행하는 머신러닝코드입니다. 여러 유형의 노트북 인스턴스의 실행시간을 측정하기 위해 쓰인 코드입니다.

- [Tensorflow SampleCode](https://github.com/op2gs2/CloudComputing_Project/blob/main/classification_Tensorflow_sample.ipynb): 이미지 분류를 수행하는 Tensorflow 샘플코드입니다. 노트북 인스턴스 환경에서 Tensorflow의 구동여부를 확인하기 위해 쓰인 코드입니다. [Tensorflow 공식홈페이지](https://www.tensorflow.org/tutorials/keras/classification?hl=ko)에서 가져왔습니다.

- [Pytorch SampleCode](https://github.com/op2gs2/CloudComputing_Project/blob/main/optimization_tutorial_Pytorch_sample.ipynb): 구한 모델을 최적화하는 Pytorch 샘플코드입니다. 노트북 인스턴스 환경에서 Pytorch의 구동여부를 확인하기 위해 쓰인 코드입니다. [Pytorch 공식홈페이지](https://tutorials.pytorch.kr/beginner/basics/optimization_tutorial.html)에서 가져왔습니다.

- 마켓플레이스 알고리즘과 데이터셋
<b> TODO: 작성 필요 </b>
  - [알고리즘](https://aws.amazon.com/marketplace/pp/prodview-vcfitb65ln2ro?sr=0-1&ref_=beagle&applicationId=AWS-Marketplace-Console):
  - [데이터셋](https://www.kaggle.com/mlg-ulb/creditcardfraud): 

## 테스트 결과 소개

### 다양한 인스턴스에서의 실행시간 비교

<b> TODO: 작성 필요 </b>

### 다양한 라이브러리 샘플코드를 실행

<b> TODO: 작성 필요 </b>

### 마켓플레이스 알고리즘을 이용한 모델 훈련

<b> TODO: 작성 필요 </b>

## 개발 결과물의 필요성 및 활용 방안

저희는 본 서비스를 다른 사람에게 소개하고, 샘플 소스코드를 가져와서 직접 구동하며 시연하는
프로젝트를 진행하였습니다. 본 프로젝트는 AWS SageMaker 상에서 개발하고, 가상머신을
구동하는, 다양한 기능을 소개하는데 그 목적이 있습니다. AWS SageMaker 에는 ML 개발에 필요한
다양한 도구들이 있습니다. 따라서 이 도구들을 사용하게끔 유도하여, 다른 이들이 더 효율적인
코딩/개발을 할 수 있도록 도움이 될 것입니다. 다른 학우들에게, 지금 배웠던 내용과는 다른, 또 다른
서비스를 소개합니다. 이를 통해, 클라우드에 대한 이해도가 증가할 수 있을 것입니다.
최근 들어, 머신러닝과 같은 인공지능은 다양한 분야에서 사용되고 있습니다. 본 도구는 인공지능을
개발하는 도구이므로, 인공지능 개발과 관련한 다양한 분야에서 쓰일 수 있을 것입니다. 
