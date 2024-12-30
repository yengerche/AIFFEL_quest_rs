# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 윤수영
- 리뷰어 : 이창민


# PRT(Peer Review Template)
- [O]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - 문제에서 요구하는 최종 결과물이 첨부되었는지 확인
        - 중요! 해당 조건을 만족하는 부분을 캡쳐해 근거로 첨부
        - 프로젝트에서 요구하는 바와 같이 데이터 전처리, 모델 학습 및 바운딩 박스 detect, 점수 도달까지 완료했다.
        - <img width="537" alt="스크린샷 2024-12-30 오전 10 46 58" src="https://github.com/user-attachments/assets/4e215dbb-a015-4d35-aaac-6595845bedb0" />
        - <img width="836" alt="1 0" src="https://github.com/user-attachments/assets/69193976-1b81-4679-8097-3b8f44ab6559" />
        - <img width="426" alt="1 1" src="https://github.com/user-attachments/assets/68237e61-1be9-4187-801c-94d0d11b12d6" />
        - <img width="718" alt="스크린샷 2024-12-30 오전 10 48 55" src="https://github.com/user-attachments/assets/ba5cd199-0ba7-40c3-bc01-e170ffd71b67" />





    
- [O]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - 해당 코드 블럭을 왜 핵심적이라고 생각하는지 확인
    - 해당 코드 블럭에 doc string/annotation이 달려 있는지 확인
    - 해당 코드의 기능, 존재 이유, 작동 원리 등을 기술했는지 확인
    - 주석을 보고 코드 이해가 잘 되었는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
        - 
        
- [O]  **3. 에러가 난 부분을 디버깅하여 문제를 해결한 기록을 남겼거나
새로운 시도 또는 추가 실험을 수행해봤나요?**
    - 문제 원인 및 해결 과정을 잘 기록하였는지 확인
    - 프로젝트 평가 기준에 더해 추가적으로 수행한 나만의 시도, 
    실험이 기록되어 있는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
        - detection에서 과적합을 확인하기 위해 epoch 별 결과를 비교 분석 진행 (5/7/49/50)
        - <img width="828" alt="스크린샷 2024-12-30 오전 10 50 45" src="https://github.com/user-attachments/assets/9c994791-42ae-494b-9731-a179ced528a6" />
        - <img width="797" alt="스크린샷 2024-12-30 오전 10 51 08" src="https://github.com/user-attachments/assets/c0889050-5cca-4a08-9065-92168c5db7d7" />



        
- [O]  **4. 회고를 잘 작성했나요?**
    - 주어진 문제를 해결하는 완성된 코드 내지 프로젝트 결과물에 대해
    배운점과 아쉬운점, 느낀점 등이 기록되어 있는지 확인
    - 전체 코드 실행 플로우를 그래프로 그려서 이해를 돕고 있는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
        - 3번에서 한 추가 실험을 통해 이번 프로젝트 분석 및 회고 진행
        - <img width="828" alt="스크린샷 2024-12-30 오전 10 50 45" src="https://github.com/user-attachments/assets/cbdd835b-784a-4f7a-b103-b4b8eacd7523" />
        - <img width="737" alt="스크린샷 2024-12-30 오전 10 53 31" src="https://github.com/user-attachments/assets/9d32b410-2c28-40d0-9a77-1b8d5a046eb1" />
        - <img width="521" alt="스크린샷 2024-12-30 오전 10 53 50" src="https://github.com/user-attachments/assets/d8c26e02-30a9-49d9-b824-2ac003c38d61" />
        - <img width="797" alt="스크린샷 2024-12-30 오전 10 51 08" src="https://github.com/user-attachments/assets/20883e18-8348-4f2c-921d-6fd7a80b3664" />





        
- [O]  **5. 코드가 간결하고 효율적인가요?**
    - 파이썬 스타일 가이드 (PEP8) 를 준수하였는지 확인
    - 코드 중복을 최소화하고 범용적으로 사용할 수 있도록 함수화/모듈화했는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
        - 최종 결과물을 제시하는 코드를 간결하고 효율적으로 구현함
        - <img width="718" alt="스크린샷 2024-12-30 오전 10 48 55" src="https://github.com/user-attachments/assets/29a3776e-0f8e-481d-b778-519728d71ff7" />





# 회고(참고 링크 및 코드 개선)
```
무려 이틀이나 모델 학습을 진행해서 학습 추이 및 주요 에포크의 결과를 정량/정성적으로 평가한 부분이 인상깊었다.
과대 적합이나 과소 적합에 해당하는 결과에 대해서 차이를 확인할 수 있었다는 점이 좋았다. (bbox, hooking 성능 등)

```
