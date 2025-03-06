# 📚 스터디 템플릿

## 📖 목차를 읽기 전에 든 생각
- 책을 처음 봤을 때 들었던 기대나 궁금증을 적어주세요.
- 이 책에서 배우고 싶은 점을 간단히 작성합니다.

## 📝 내용 정리
#### 도커 아키텍처

![Docker Architecture ](https://media.geeksforgeeks.org/wp-content/uploads/20221205115118/Architecture-of-Docker.png)

**Client** : docker cli (명령어 입력 Docker run .. )

**Docker Daemon** : 도커와 관련된 리소스를 관리하는 백그라운드 프로세스

**Docker Registry** : github 같이 이미지들을 보관할 수 있는 저장소



#### 도커 이미지 관련 명령어

| 명령어               | 설명                             |
| -------------------- | -------------------------------- |
| docker image build   | Dockerfile로 부터 이미지 빌드    |
| docker image history | 이미지 히스토리 확인             |
| docker image ls      | 이미지 목록 확인                 |
| docker image prune   | 사용하지 않는 이미지 삭제        |
| docker image pull    | 레지스트리로부터 이미지 다운로드 |
| docker image push    | 레지스트리로 이미지 업로드       |
| docker image tag     | 이미지 태그를 생성               |

#### 도커 컨테이너 관련 명령어

| 명령어                   | 설명                                          |
| ------------------------ | --------------------------------------------- |
| docker container commit  | 변경된 컨테이너에 대한 새로운 이미지 생성     |
| docker container attach  | 실행중인 컨테이너의 표준 입출력 스트림에 붙음 |
| docker container exec    | 실행중인 컨테이너에 명령어를 실행             |
| docker container inspect | 하나 이상의 컨테이너의 자세한 정보를 표시     |
| docker container prune   | 멈춰있는 모든 컨테이너를 삭제                 |
| docker container restart | 하나 이상의 컨테이너를 재실행                 |
| docker container rm      | 하나 이상의 컨테이너를 삭제                   |
| docker container run     | 이미지로부터 컨테이너를 생성하고 실행         |





## 💡 전부 읽고 난 후기
- 책을 다 읽고 난 후 느낀 점, 배우게 된 점, 아쉬운 점을 자유롭게 적어주세요.
- 전체적인 평가나 적용하고 싶은 점도 포함될 수 있습니다.

## ❓ 특별히 궁금했던 부분
- 읽으면서 생겼던 의문이나 더 탐구하고 싶은 부분을 정리합니다.
- 팀원들과 논의하고 싶은 내용을 포함해도 좋습니다.

## ⏳ 독서 과정 기록
- **총 독서 시간**: (예: 3시간 20분)
- **각 장별 소요 시간**:
  - Chapter 1: (예: 40분)
  - Chapter 2: (예: 1시간)
  - ...

## 🤔 이해도 점검 & 난이도 평가
- **어려웠던 부분 & 이유**:
  - 이해가 어려웠던 개념이나 문장이 있다면 적어보세요.
  - 왜 어려웠는지(배경지식 부족, 개념이 생소함 등) 생각해 봅니다.

- **자신의 이해도를 점수로 표현하기 (5점 만점)**
  - Chapter 1: ⭐⭐⭐☆☆ (3/5)
  - Chapter 2: ⭐⭐⭐⭐☆ (4/5)

- **특별하게 깨달음을 얻은 부분**
  - 이해하기가 어려웠던 이유가 무엇 때문이었는지, 이 부분이 핵심이라고 생각되는 부분을 적어주세요.