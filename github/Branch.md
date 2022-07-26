# Branch
분기된 가지 (다른 차원)
- 프로젝트를 하나 이상의 모습으로 관리해야 할 때
- 여러 작업들이 각각 독립되어 진행될 때

## 브랜치 생성 / 이동 / 삭제

브랜치 생성
```
git branch {branch}
```

브랜치 목록 확인
```
git branch
```

브랜치로 이동
```
git swich {branch}
```
- `checkout` 명령어가 git 2.23 버전부터 `switch`, `restore`로 분리

브랜치 생성과 동시에 이동
```
git switch -c new-teams
```
- 기존의 `git checkowt -b {branch}`

브랜치 삭제하기
```
git branch -d {branch}
```

(지워질 브랜치에만 있는 내용의 커밋이 있을 경우)
```
git branch -D {branch}
```

브랜치 이름 바꾸기
```
git branch -m {기존 브랜치} {새 브랜치}
```

## 각각의 브랜치에서 서로 다른 작업해보기

여러 브랜치의 내역 편리하게 보기
```
git log --all --decorate --oneline --graph
```

## branch를 합치기

### merge: 두 브랜치를 한 커밋에 이어붙인다. (history가 남음)

- `add-coach` 브랜치를 `master` 브랜치로 merge
- `master` 브랜치로 이동
```
git merge add-coach
```
- 병합된 브랜치는 삭제

merge는 reset으로 되돌리기 가능

### rebase: 브랜치를 다른 브랜치에 이어붙인다. (history가 남지 않음)

- `new-teams` 브랜치를 `main` 브랜치로 rebase
- `new-teams` 브랜치로 이동 (`merge` 때와는 반대)
```
git rebase master
```
- `main` 브랜치로 이동 후 아래 명령어로 `new-teams`의 시점으로 fast-forward
```
git merge new-teams
```
- `new-teams` 브랜치 삭제

## 충돌 해결하기

### `merge` 충돌 해결하기

당장 충돌 해결이 어려울 경우 `merge` 중단
```
git merge --abort
```

해결 가능 시 충돌 부분을 수정한 후 병합 완료

### `rebase` 충돌 해결하기

당장 충돌 해결이 어려울 경우 아래 명령어로 `merge` 중단

해결 가능 시
- 충돌 부분을 수정한 뒤 `git add .`
- 아래 명령어로 계속
```
git rebase --continue
```
- 충돌이 모두 
