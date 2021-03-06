## GitHub 레포지토리 생성 후 복붙

```
git remote add origin {https protocol}
```
- 로컬의 git 저장소에 원격 저장소로의 연결 추가
  - 원격 저장소 이름에 흔히 `origin` 사용

```
git branch -M main
```
- GitHub 권장: 기본 브랜치명을 `main` 으로

```
git push -u origin main
```
- 로컬 저장소의 커밋 내역들 원격으로 `push`
  - `-u` 또는 `--set-upstream`: 현재 브랜치와 명시된 원격 브랜치 기본 연결

원격 목록 보기
```
git remote
```

자세히 보기
```
git remote -v
```

원격 지우기 (로컬 프로젝트와의 연결 끊기)
```
git remote remove {remote repository name}
```

## GitHub에서 프로젝트 다운받기

터미널로 대상 폴더 이동 후
```
git clone {https protocol}
```

## pull 할 것이 있을 때 push를 하면?

1. merge 방식
```
git pull --no-rebase
```

2. rebase 방식
```
git pull --rebase
```

이후 push하기

## 원격의 브랜치 다루기

### 로컬에서 브랜치 만들어 원격에 push하기

  1. `from-local`브랜치 만들기
  2. 아래 명령어로 원격에 `push`
  ```
  git push -u origin from-local
  ```
  3. 브랜치 목록 살펴보기
  ```
  git branch -all
  ```
  
### 원격의 브랜치 로컬에 받아오기

  1. 아래 명령어로 원격의 변경사항 확인
  ```
  git fetch
  ```
  2. 아래 명령어로 로컬에 같은 이름의 브랜치를 생성하여 연결하고 switch
  ```
  git switch -t origin/from-remote
  ```
  
### 원격의 브랜치 삭제

```
git push {원격 이름} --delete {원격의 브랜치명}
```
