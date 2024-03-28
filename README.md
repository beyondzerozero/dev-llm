# dev-llm

이 리포지토리는 LLM을 조정하는데 사용되는 Docker이미지를 만드는데 목적을 둔다. 환경구축의 어려움을 겪는 독자가 LLM튜닝을 용이하게 시작할 수 있도록 도와주는 것을 목표로 한다. 또한, Docker를 사용할 수 없는 환경용으로 pyenv용도 작성해두었기 때문에 ABCI등을 이용하는 경우도 사용 가능하다.

## 1. 준비

LLM 환경을 구축하려면 우선 Docker가 필요하다. Docker를 설정하는 방법에 대한 자세한 내용 [NVIDIA Docker](https://github.com/NVIDIA/nvidia-docker)를 참고하기 바란다.

## 2. 이미지 빌드

Docker환경을 준비한 후, LLM용 Docker 이미지를 빌드한다. 다음 단계를 따르자.

```bash
git clone https://github.com/beyondzerozero/dev-llm.git # 이 저장소에 복사
cd dev-llm/docker
./build.sh # 이미지 빌드
```

실행권한이 없으면 `chmod` 명령을 사용하여 알맞은 권한을 부여한다. 이 단계에서 시간이 많이 걸릴 수 있다.

## 3. Docker 이미지 사용

Docker 이미지에서 컨테이너를 설정하려면 다음 명령을 실행한다.

```bash
docker compose up
```

### JupyterLab 접속

위 명령을 실행하면 JupyterLab이 시작된다. 로컬에서 실행중인 경우, 브라우저에서 localhost:8888로 접속하자. 원격PC로 환경을 실행하는 경우 해당 PC의 IP다음 :8888 포트번를 지정해서 브라우저에서 접속하자.
