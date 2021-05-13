# 🌱 Git의 기초
### 🗑 저장소에 관한 명령어
- **git 저장소 만들기**
```bash
$ git init
# 해당하는 폴더에 .git이라는 디렉토리가 생성되며, 해당 폴더가 Git local repository로 지정된다.
```

- **git init 취소 명령어**

```bash
$ rm -r .git
# 위 명령을 통해 만든 .git 디렉토리를 제거 하면 git local repository 지정을 해제하게 된다.
```

### 🛎 스테이징 명령어

```bash
$ git add [file/dir경로]  # 작업 디렉토리의 변경 내용의 일부만 스테이징 영역으로 넘기고 싶을 때
$ git add .   # 현재 디렉토리의 모든 변경 내용을 스테이징 영역으로 넘기고 싶을 때
$ git add -A  # 작업 디렉토리 내의 모든 변경 내용을 스테이징 영역으로 넘기고 싶을 때
```

- **git add 취소 명령어**

```bash
$ git reset HEAD [file]  # 특정 파일 add 취소
$ git reset  # 전체 파일 add 취소
```

### 📟 Commit 명령어

```bash
$ git commit -m "커밋메세지"
```

- **git commit 취소 명령어**

```bash
$ git reset --soft HEAD^  # 가장 최근 commit만 취소
$ git reset HEAD^         # 가장 최근 commit,add 취소 [기본 옵션]
$ git reset --hard HEAD^  # 가장 최근 commit,add 취소를 한 다음 Work Space에서 삭제
$ git reset HEAD~2        # 마지막 2개의 commit을 취소
```

- **git commit message 변경 명령어**

```bash
$ git commit --amend
```

### ⏱ 이전 커밋으로 되돌리는 명령어

```bash
$ git reset <옵션> <돌아가고싶은 커밋>
```

#### 😎 옵션 종류

**1. hard**
```bash
$ git reset --hard <돌아가고싶은 커밋>
# 돌아가려는 이력이후의 모든 내용을 지워 버립니다. 
```
**2. soft**
```bash
$ git reset --soft <돌아가고싶은 커밋>
# 돌아가려 했던 이력으로 되돌아 갔지만, 이후의 내용이 지워지지 않고, 해당 내용의 스테이징도 그대로 되어있다.
# 바로 다시 커밋할 수 있는 상태로 남아있는 것
```
**3. mixed** (옵션을 적지 않으면 mixed로 동작)
```bash
$ git reset --mixed <돌아가고싶은 커밋>
# 역시 이력은 되돌려진다. 이후에 변경된 내용에 대해서는 남아있지만, 스테이징은 초기화
# 커밋을 하려면 다시 변경된 내용은 추가해야 하는 상태
```
**4. HEAD~N**
```bash
git reset HEAD~6
# 위와 같이 현재부터 6개 이전 이력으로 돌아가라라고 상대적으로 지정 가능
```