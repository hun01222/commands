## 저장소 생성
 
- 원하는 폴더 들어간 후

```
git init
```

## 코드 생성

- README 라는 파일에 스트링 문자 생성

```
echo "Hello, Git!" > README.md
```

## Staging 영역에 추가

- 현재 디렉토리에 업데이트된 파일 모두 추가

```
git add .
```

- 수정된 파일 모두 스테이징 영역 추가

```
git add -A
```

- 현재 add 내역 확인

```
git status
```

## Repository 에 commit

```
git commit -m "Hello"
```
**commit = 버전 = 타임캡슐**

## 원격저장소에 push, 업데이트된 내용 가져오기는 pull

- 원격 저장소 연결

```
git remote add origin URL
```

- 원격 저장소 제거

```
git remote remove origin
```

- push

```
git push origin master
```

 - push 가 안되면 강제로 push
 
 ```
 git push origin +master
 ```

- 상대방 업데이트 된 내용 받아오기

```
git pull
```
