## Langgraph

### 2024-05-15

![아키텍처3](./images/image4.png)

- 매번 크롤링하는것은 비효율적이기떄문에 이미 해당 검색어로 검색을 했었다면 저장된 정보로 추천을 진행하기 위함입니다.

### 2024-05-01

![아키텍처2](./images/image3.png)

- `python test.py` 실행으로 input을 통해 검색어를 추출하고 검색을 진행하여 음식점 이름으로만 추천을 진행합니다.

## 크롤링 구조

![아키텍처](./images/image.png)

1. 공용의 Redis 존재
2. 검색어에 따라 레스토랑 목록을 크롤링 해서 Redis에 저장
3. Redis의 데이터를 각자의 VM에서 하나씩 가져와서 처리 후 공용 Storage 혹은 DB에 저장

### 동시성제어 테스트

https://github.com/ehddnr301/crawling_example/assets/54092915/326bcdb0-09d2-47c7-8017-c98ed848a874
