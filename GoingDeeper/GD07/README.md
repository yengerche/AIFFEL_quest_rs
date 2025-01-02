# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 윤수영
- 리뷰어 : 김준석

# PRT(Peer Review Template)
- [O]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - 문제에서 요구하는 최종 결과물이 첨부되었는지 확인
        - 중요! 해당 조건을 만족하는 부분을 캡쳐해 근거로 첨부  
    1. U-net을 통한 세그멘테이션 작업이 정상적으로 진행되었습니다.  
       <img width="695" alt="image" src="https://github.com/user-attachments/assets/dfa3112a-3714-4aef-9f34-76272f7b5ddd" /><br>
       <img width="690" alt="image" src="https://github.com/user-attachments/assets/d2fe48f3-6954-446f-9176-b22b94fba36d" /><br>

    2. U-net++ 모델이 성공적으로 구현되었습니다.  
       <img width="608" alt="image" src="https://github.com/user-attachments/assets/9e491e50-96fb-4fc2-81d8-897652182d1e" /><br>

    3. U-net과 U-net++ 두 모델의 성능이 정량적/정성적으로 잘 비교되었습니다. 특히 3가지 모델에 대한 실험을 바탕으로 비교한 점이 훌륭하다고 생각합니다.  
       <img width="583" alt="image" src="https://github.com/user-attachments/assets/709671d0-4e94-41d8-8878-83abd1e386e2" /><br>
       <img width="586" alt="image" src="https://github.com/user-attachments/assets/44b1c454-6eb6-4d3a-be19-bcd142414abe" /><br>
       <img width="565" alt="image" src="https://github.com/user-attachments/assets/93ae6326-c110-493c-b372-6b35f2486637" /><br>
       <img width="569" alt="image" src="https://github.com/user-attachments/assets/43343b00-dfc2-4a0a-a81d-dc6db47bf268" /><br>
       <img width="590" alt="image" src="https://github.com/user-attachments/assets/f600f60a-108f-480f-b1f2-f2127c49d7e4" /><br>

       
- [O]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - 해당 코드 블럭을 왜 핵심적이라고 생각하는지 확인
    - 해당 코드 블럭에 doc string/annotation이 달려 있는지 확인
    - 해당 코드의 기능, 존재 이유, 작동 원리 등을 기술했는지 확인
    - 주석을 보고 코드 이해가 잘 되었는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부  
        -> 실제 U-net++ 모델은 중간레이어의 출력도 손실함수 계산에 포함됩니다. 이를 파악하여 실제로 모델로 구현해보려고 한 점이 좋았습니다.  
          <img width="668" alt="image" src="https://github.com/user-attachments/assets/a75d04eb-5a50-4990-b676-3446e1f897d4" /><br>


- [O]  **3. 에러가 난 부분을 디버깅하여 문제를 해결한 기록을 남겼거나
새로운 시도 또는 추가 실험을 수행해봤나요?**
    - 문제 원인 및 해결 과정을 잘 기록하였는지 확인
    - 프로젝트 평가 기준에 더해 추가적으로 수행한 나만의 시도, 
    실험이 기록되어 있는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부  
        -> 손실함수 계산에 대한 다양한 실험을 진행한 뒤, 각각 정량적 정성적 비교를 한 점이 잘 작성되었다고 생각합니다.  
          (상단, Only final loss, loss voting1, loss voting2 참조)
     

- [O]  **4. 회고를 잘 작성했나요?**
    - 주어진 문제를 해결하는 완성된 코드 내지 프로젝트 결과물에 대해
    배운점과 아쉬운점, 느낀점 등이 기록되어 있는지 확인
    - 전체 코드 실행 플로우를 그래프로 그려서 이해를 돕고 있는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부  
        -> 결과에 대한 회고를 잘 작성하였습니다.  
          <img width="601" alt="image" src="https://github.com/user-attachments/assets/53095802-e168-4f94-a262-109719541bad" /><br>

        
- [O]  **5. 코드가 간결하고 효율적인가요?**
    - 파이썬 스타일 가이드 (PEP8) 를 준수하였는지 확인
    - 코드 중복을 최소화하고 범용적으로 사용할 수 있도록 함수화/모듈화했는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부  
          -> 리뷰어 입장에서 리뷰하기 쉽게 결과분석용 파일을 잘 만들어 주셨습니다.  


# 회고(참고 링크 및 코드 개선)
```
수영님 덕분에 저도 놓쳤던 부분을 파악하고 공부할 수 있었습니다. 감사합니다ㅎㅎ 고생많으셨습니다!
```
