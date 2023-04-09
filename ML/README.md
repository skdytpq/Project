# ML_Predict-survey-responses

### 설문조사 응답 여부 예측
1. 설문 항목별로 다양한 값이 존재했기 때문에 값의 scale을 맞춰주기 위해 임의의 범위 내로 값을 scaling함
2. 다양한 feature를 생성하여 예측 성능 향상을 이룸
3. `shap` 패키지를 사용한 Feature Selection으로 모델 성능에 효과적인 파생변수만 선택
4. 각각 RandomSearch, Optuna 등을 활용한 hyper-parameter tuning을 통해 모델 성능을 향상하고자 함
5. 각각의 모델 output에 대한 submission ensemble을 통해 최종적인 모델 성능을 향상시킴


< 진행 예시 >

<img width="1108" alt="image" src="https://user-images.githubusercontent.com/87609200/215307262-501215de-a6f6-4b64-bc6a-676c09073bc8.png">


### 느낀점  
* 설문 문항 전처리 및 다양한 파생변수를 생성하며 output을 출력하면서 다양한 기법들이 ML에서 적용될 수 있다는 것을 느낌
  * Data Preprocess,  Feature Extraction, Feature Selection, Encoding, Scaling ...
* 시계열 예측에 있어서 과거 시점의 데이터를 학습시켜 최근의 데이터를 test해야 된다는 시계열 분석 기법을 배움
  * 사회적으로 통용되는 개념을 ML에 적용했더니 성능이 오르는 것을 보아 엔지니어의 insight가 결과 도출에 큰 영향을 미친다는 것을 느낌
* 앙상블 기법은 모델 성능을 올리는데 큰 기여를 할 수 있으나, 전체적인 model capacity가 증가하여 실무에서도 잘 사용되는지 궁금증이 생김
