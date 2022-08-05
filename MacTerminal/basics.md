## 절대경로와 상대경로

- 절대경로: `users/Home/Applications` 와 같이 나타낸다. 원하는 폴더를 drag and drop 해도 가능! `cd /` 는 사용자의 폴더 중 제일 상위 단계 폴더로 이동 가능하다.
- 상대경로: 본인의 위치를 `.` 부모의 위치를 `..` 으로 한다.

## 파일, 디렉토리 관련

- home directory `~`
- current path `pwd`
- list of directory `ls`
- go to directory `cd`
- open file `open {file name}`
- make file
  - `cat > {file name}` : 파일을 생성하면서 데이터를 입력
  - `touch` : 빈 파일을 생성하거나 수정시간을 변경
- make directory `mkdir {folder name}`
- delete directory `rm -r {folder name}`
- delete directory as recursive force `rm -rf {folder name}`
- delete file `rm`
- catenate (어떤 내용을 터미널 화면에 뿌린다.) `cat [filename]`
- copy `copy {file} {directory}`
- move A to B `mv {A} {B}`
- source (스크립트 파일을 수정한 후 수정된 값을 바로 적용하기 위해 사용하는 명령어) `source {file}`

## 특수 문자 관련

|특수문자|사전정의|
|----|----|
|#|주석|
|$|쉘 변수|
|&|백그라운드 작업|
|*|문자열 와일드 카드|
|?|한 문자 와일드 카드|
|[]|문자의 범위를 지정|
|;|쉘 명령 구분자|
|||파이프|
|<|입력 재지정|
|>|출력 재지정|
|>>|출력 재지정 (이어쓰기)|
|&&|이전 명령이 정상 종료인 0의 값을 반환할 경우에만 다음 명령 실행|
||||이전 명령이 비정상 종료인 1의 값을 반환할 경우에만 다음 명령 실행|

## 환경 변수 관련
