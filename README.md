# 딥러닝을 활용한 한국 음식 이미지 데이터 분류

## 프로젝트 개요
| 한식 이미지 데이터를 분류하는 모델을 만들었습니다!

양식에 대한 이미지 데이터를 분류 하는 모델 구현은 깃허브에 많이 존재 했지만, 한식을 분류하는 모델은 없어서 구현하기로 했습니다. AIHUB에서 제공하는 한식 이미지를 다운 받아서 대표적인 한식 30가지 1000개의 이미지 데이터를 학습 시켜 보았습니다. 'inceptionV3 model을 활용하여 한식에서도 양식과 같이 이미지를 분류 할 수 있다'라는 가설을 세우고 가설을 검증하는 과정을 진행했습니다.



## 프로젝트 목표
- 가설검증
- 모델 구현 후 구글에 있는 한식 이미지로 테스트


## 프로젝트 결과
| 검증 데이터 정확도 88%의 이미지 분류 모델을 구현했습니다!


##Train/Valid Data
- AIHUB 한국 음식 이미지


## Test Data
- 구글에 있는 한식 이미지


## Model Summary
- 인셉션 모델 밑단에 flatten과 dense층 넣어 전이 학습 구현
- inceptionV3
- Flatten()
- Dense()

## Model Result
![image](https://user-images.githubusercontent.com/71398226/133580125-72e7808d-78e7-43ab-bc73-4bcbfd8e3cf3.png)

loss: 0.5929 - acc: 0.8845 val_loss, val_acc: [0.5929082036018372, 0.8845233917236328]

## Model Prediction

### 삼겹살
![image](https://user-images.githubusercontent.com/71398226/133580317-265bb2a0-4070-4ebd-aca1-81c5a1e7d2e6.png)
![image](https://user-images.githubusercontent.com/71398226/133580333-fcbfcae3-d605-486e-be16-690f99ba1e8a.png)


### 삼계탕
![image](https://user-images.githubusercontent.com/71398226/133580391-20e6386c-d86a-44c0-b2a7-bc4459d9ad7d.png)
![image](https://user-images.githubusercontent.com/71398226/133580404-c1909e50-adc9-4c7f-bcd5-2f5e4aa2daf0.png)

---

## 모델 한계
- 모델의 정확도는 88%지만, 테스트 이미지를 넣어 봤을 때 생각보다 성능이 좋지 않았음
- 능력 부족으로 150종의 한식 대신 30종의 한식만 추려서 학습
- 음식이 여러개 나온 경우 정확도가 급격하게 떨어짐


## 추후 해결할 문제
- 음식 사진을 먼저 YOLO 모델을 활용하여 인식후, Cropping 하여 이미지 분류 (여러개의 음식사진 때문)
- 더 큰 이미지 데이터들을 다룰 수 있는 능력 향상
- Image generator에 대한 이해도 상승 요구
