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



### 도커 컨테이너 네트워크

```shell
docker network ls
```

##### bridge

> 컨테이너 생성 시 기본으로 제공하는 드라이버
>
> 각 컨테이너는 각자의 네트워크 인터페이스를 가지고, 이는 도커 호스트의 docker0와 바인딩 됨

##### host

> 컨테이너 생성 시 컨테이너 자체적으로 네트워크 인터페이스를 가지지 않고 호스트 네트워크 인터페이스를 공유함
>
> 컨테이너 실행시 --network=host 를 사용해서 실행 

##### none

> 실행한 컨테이너가 네트워크 인터페이스를 가지지 않아 컨테이너 외부와의 통신이 불가함
>
> 컨테이너 실행 시 --network=none을 사용해서 실행

### 호스트 - 컨테이너 간 파일 전송

호스트 -> 컨테이너

```shell
docker container cp {호스트 파일 위치} {docker container id}:{복사할 위치}
```

컨테이너 -> 호스트

```shell
docker container cp {docker container id}:{복사할 위치} {호스트 파일 위치}
```

### 도커 스토리지

> 도커 컨테이너는 삭제가 되면 컨테이너 내부에 존재하는 파일들도 같이 사라짐. 
>
> 데이터를 보존하기 위해 도커 스토리지를 사용

![Docker for Beginners: Understanding Docker Storage and Volumes](https://www.iamachs.com/p/docker/part-5-understanding-docker-storage-and-volumes/docker-storage.png)

파일을 저장하는 방식에는 세가지 방식이 존재한다. 

- bind mount : 도커 호스트 디렉터리를 직접 공유하는 방식
- volume : 도커를 활용해 볼륨을 생성한 후 컨테이너의 디렉터리와 공유하는 방식
- tmps : 도커 호스트 메모리에 파일이 저장되는 방식 (컨테이너가 삭제되면 해당 파일도 삭제됨)

## 💡 전부 읽고 난 후기
- 도커에 대한 세부적인 내용들을 알 수 있어 좋았다.

## ❓ 특별히 궁금했던 부분
- 실제 업무에서 Bind mount 혹은 volume에 데이터를 보관해야 하는 일이 존재할 까?

## ⏳ 독서 과정 기록
- **총 독서 시간**: 1h 30
- **각 장별 소요 시간**:
  - Chapter 2: 1h 30

## 🤔 이해도 점검 & 난이도 평가
- **어려웠던 부분 & 이유**:
  - 다소 어려웠던 내용은 딱히 없었던 것 같다.
  
- **자신의 이해도를 점수로 표현하기 (5점 만점)**
  - Chapter 2: ⭐⭐⭐⭐⭐
  
- **특별하게 깨달음을 얻은 부분**
  - 도커 네트워크에 대한 개념을 어렴풋이나마 알게 될 수 있었다.