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

`master` 브랜치로 이동
`add-coach` 브랜치를 `master` 브랜치로 merge
```
git merge add-coach
```

merge는 reset으로 되돌리기 가능

### rebase: 브랜치를 다른 브랜치에 이어붙인다. (history가 남지 않음)

`new-teams` 브랜치를 `main` 브랜치로 rebase
