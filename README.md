# CNN_X_LSTM_smartfactory



## Members
- **김유선**(School of Mechanical Engineering, Chung-Ang Univ)
- **신선우**(College of Art and Technology, Chuna-Ang Univ)
- **유찬재**(School of Mechanical Engineering, Chung-Ang Univ)
- **최연찬**(School of Mechanical Engineering, Chung-Ang Univ)

## Abstract
CNN의 ResNet50, RNN의 LSTM을 활용해 모델을 구축하고 학습시킨다. 이 후 하이퍼 파라미터(batch_size, learning_rate, dropout_rate)의 변화를 준 뒤, 각 시행 별로 나오는 Test & Validation Error의 변화 그래프를 고찰 및 분석한다.

## Topic 
농업 환경 변화에 따른 작물 병해 진단 AI

## Data
Dacon(https://dacon.io/competitions/official/235870/data)의 데이터 셋 활용

## 참고 자료
[parameter_analysis.docx](https://github.com/CUAI-CAU/CNN_X_LSTM_smartfactory/files/8001235/parameter_analysis.docx)

## Conclusion
1.	Batch size가 1일 때와 8일 때를 비교해 보면, Batch size가 큰 경우 train error이 전반적으로 낮게 측정이 되는 것을 알 수 있습니다. 따라서 성능을 극대화할 수 있는 Batch size의 크기를 찾고 학습을 진행하는 것이 모델의 성능을 향상시키는데 중요한 요소일 것입니다.

2.	Drop out rate의 경우, Batch size가 1일 때에는 0일 때가 가장 우수하였고, Batch size가 8일 때에는 0.1일 때가 가장 우수하였습니다. 이를 통하여 배치 사이즈는 적절한 수치를 잘 찾는 것이 좋다는 것을 알 수 있었습니다. 더욱 정확한 상황 판단을 위하여 train error, validation error, test error 그래프를 잘 확인하여 분석하면 될 것입니다.

3.	Batch size가 8일 때에는 Learning rate의 경우에 전반적으로 값이 낮을수록 유리하였지만, Batch size를 1로 학습을 시켰을 때에는 유의미한 상관관계가 없었습니다. Batch size가 가중치 업데이트에 참조되는 sample의 개수이기 때문에, 적절한 배치사이즈의 크기는 학습에 중요한 요소인 것을 확인하였습니다.

