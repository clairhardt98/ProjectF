# 개발 일지

---

### 230606

1. 개발 시작
    1. base 브랜치 생성
        1. base 브랜치에서 기본적인 틀 작업중
2. Player 오브젝트 생성
    1. Player 이동 구현
        
        ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/78a85292-7867-4256-a137-f416e24aa555/Untitled.png)
        
        - 이동 속도부터 구한다
        - Player 오브젝트 variable에 Speed생성 후 플레이어가 가질 속도 값 지정
        - Get Axis 노드로 수평방향 입력(좌, 우)를 입력받음 : 각각 -1, 1
        - 이동속도와 입력받은 값을 곱하여 graph variable인 Movement에 입력
        
        ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ae030833-3534-46ca-8fc5-b4e3ed22648e/Untitled.png)
        
        - Get Velocity에 self로 인자 지정하여 현재 이 오브젝트의 이동속도 참조
            - 현재 Player 오브젝트의 y속도는 0이므로 0 반환
        - graph variable인 movement의 값과 위에서 구한 y속도를 토대로 2D벡터 생성,
        - set velocity를 통해 Player에게 생성한 2D벡터 속도 전달
