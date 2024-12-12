# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 윤수영
- 리뷰어 : 김영민


# PRT(Peer Review Template)
- [ ]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - 문제에서 요구하는 최종 결과물이 첨부되었는지 확인
        - 중요! 해당 조건을 만족하는 부분을 캡쳐해 근거로 첨부
    - 학습이 완료되지 않아서 결과를 볼 수 없지만 코드상 오류가 난 부분이 없고 코드 진행에도 꼬인 부분이 없어 기대하는 결과가 나올 것으로 기대됩니다.
        ![코드](https://github.com/user-attachments/assets/c20aa66b-3885-4d08-bfd9-7246a59f59bc)
```python
def build_plain_block(input_layer,
                      filter_sizes = [3, 3],
                      channels=[64, 64],
                      loof_num =1,
                      block_num=1,
                      resd_num = 1,
                      residual = False,
                     ):
    
    # 입력 레이어
    x = input_layer
    identity = x
    
    # CNN 레이어
    for cnn_num, (filter_size, channel) in enumerate(zip(filter_sizes, channels)):
        if block_num in [3, 4, 5]:
            if loof_num + cnn_num == 0:
                stride_num = 2
            else :
                stride_num = 1
        else :
            stride_num = 1
            
        x = keras.layers.Conv2D(
            filters=channel,
            kernel_size=(filter_size,filter_size),
            strides=stride_num,
            activation=None,
            kernel_initializer='he_normal',
            padding='same',
            name=f'block{block_num}_conv{loof_num + cnn_num + 1}'
        )(x)
        x = keras.layers.BatchNormalization()(x)
        if cnn_num != len(filter_sizes):
            x = keras.layers.Activation('relu')(x)
        
    if residual:
        if block_num in [3, 4, 5]:
            stride_num = 2
            if loof_num == 0:
                stride_num = 2
            else:
                stride_num = 1
        else :
            stride_num = 1
            
        identity = keras.layers.Conv2D(
            filters=channels[-1],
            kernel_size=(1,1),
            strides=stride_num,
            activation='relu',
            kernel_initializer='he_normal',
            padding='same',
            name=f'block{block_num}_linear_projection{resd_num}'
        )(identity)
        
        if block_num in [3, 4, 5]:
            if loof_num == 0:
                identity = keras.layers.BatchNormalization(name=f'block{block_num}_barch_shout{resd_num}')(identity)
        
        x = keras.layers.Add(name=f'block{block_num}_residual{resd_num}')([x,identity])
        x = keras.layers.Activation('relu')(x)
    
    return x
```
    
- [x]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - 해당 코드 블럭을 왜 핵심적이라고 생각하는지 확인
    - 해당 코드 블럭에 doc string/annotation이 달려 있는지 확인
    - 해당 코드의 기능, 존재 이유, 작동 원리 등을 기술했는지 확인
    - 주석을 보고 코드 이해가 잘 되었는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
    - 이번 학습에서 가장 핵심이라고 생각되는 build_block부분을 코드블럭 단위로 주석이 남겨저 있고 줄 바꿈도 유연하게 되어 있어서 가독성이 좋습니다.
```python
    # 입력 레이어
    x = input_layer
    identity = x
    
    # CNN 레이어
    for cnn_num, (filter_size, channel) in enumerate(zip(filter_sizes, channels)):
        if block_num in [3, 4, 5]:
            if loof_num + cnn_num == 0:
                stride_num = 2
            else :
                stride_num = 1
        else :
            stride_num = 1
```
        
- [x]  **3. 에러가 난 부분을 디버깅하여 문제를 해결한 기록을 남겼거나
새로운 시도 또는 추가 실험을 수행해봤나요?**
    - 문제 원인 및 해결 과정을 잘 기록하였는지 확인
    - 프로젝트 평가 기준에 더해 추가적으로 수행한 나만의 시도, 
    실험이 기록되어 있는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
    - 구현한 모델로 훈련이 충분히 가능하고 모델의 summary역시 논문의 내용과 일치하게 구성되었습니다.
    ![추가구현](https://github.com/user-attachments/assets/6e403feb-32bf-45ab-aa5d-a30f921e5144)
        
- [x]  **4. 회고를 잘 작성했나요?**
    - 주어진 문제를 해결하는 완성된 코드 내지 프로젝트 결과물에 대해
    배운점과 아쉬운점, 느낀점 등이 기록되어 있는지 확인
    - 전체 코드 실행 플로우를 그래프로 그려서 이해를 돕고 있는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
    - 부족했던점과 더 해봐야할 부분을 회고를 통해 잘 기록하였고 어떻게 이를 개선할 지 회고를 통해 분석함
    ![회고](https://github.com/user-attachments/assets/91c84862-c093-4640-829c-8bc64498a4a6)
        
- [x]  **5. 코드가 간결하고 효율적인가요?**
    - 파이썬 스타일 가이드 (PEP8) 를 준수하였는지 확인
    - 코드 중복을 최소화하고 범용적으로 사용할 수 있도록 함수화/모듈화했는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
    - 주석도 간결하게 작성되어 있고 코드가 어떻게 진행되는지 한눈에 볼 수 있습니다.
    - 데이터 분할에서도 이전 cifar-10과 달라진 데이터셋에 맞춰 효율적으로 코드를 구성해 변경하였습니다.
    


# 회고(참고 링크 및 코드 개선)
```
# 리뷰어의 회고를 작성합니다.
# 코드 리뷰 시 참고한 링크가 있다면 링크와 간략한 설명을 첨부합니다.
# 코드 리뷰를 통해 개선한 코드가 있다면 코드와 간략한 설명을 첨부합니다.
```
- 파라미터 수가 사람마다 조금씩 차이가 있습니다. 제 코드와 비교해서 어느 부분이 다른지 상세하게 분석해 볼 필요가 있을 것 같습니다.
- 파라미터 수에서 제가 작성한 코드보다 더 적은 양을 가지고 모델을 구현했습니다. 파라미터 수가 큰 차이가 나는건 아니지만 레이어구성도 고려해서 얼마나 성능의 차이가 날지 결과가 나온 후 살펴보겠습니다.
![파라미터](https://github.com/user-attachments/assets/bdc02f19-d6b1-424b-9e0a-1e06eff8497e)