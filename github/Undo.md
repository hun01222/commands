## Staging

- 전체 파일 unstaging

```
git reset HEAD
```

- staging 상태 보기

```
git status
```

## Local Repository

- 전체 파일 staging

```
git reset --soft HEAD^
```

- 전체 파일 unstaging

```
git reset --mixed HEAD^
git rest HEAD^
```

- local repository 상태 보기

```
git log -g (press Q to quit)
```

## Remote Repository

- 가장 최근의 commit 취소 후 working directory 되돌림
- 원하는 시점으로 working dirctory 되돌림 ~ ```git log -g``` 통해

- 다시 commit
- forced push

```
git reset HEAD^
git rest HEAD@{number}
```
```
git commit -m ""
```
```
git push origin +master
```
