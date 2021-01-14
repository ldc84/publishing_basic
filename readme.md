# 사이트 런칭

## 목차
> 1. git 설치
> 2. github 회원가입
> 3. git desktop 설치
> 4. 작업물 업로드

## 1. git 설치
https://git-scm.com/

### 기본 명령어
* <u>최초 먼저 웹</u>에서 저장소를 먼저 생성 후 복사해서 사용하는 경우<br>
repository 생성 후
```bash
> git remote add origin https://github.com/username/repo.git
> git branch -M main (또는 master)
> git push -u origin main (또는 master)
```

* <u>최초 먼저 로컬</u>에서 작업한 파일들을 본인 github repo에 올릴 경우<br>
repository 생성 후
```bash
> git init
> git add .
> git commit -m "msg"
> git branch -M main (또는 master)
> git remote add origin https://github.com/username/repo.git
> git push -u origin main (또는 master)
```

* 기존에 연결된 repository(저장소) 에서 최신 버전으로 업데이트 받을때
```bash
> git pull
```

* 기존에 연결된 repository(저장소) 로
```bash
> git add .
> git commit -m 'msg'
> git push
```



## 2. github 회원가입
>회원가입시 아이디가 도메인에 영향을 줄 수 있음.

https://github.com/

## 3. git desktop 설치
https://desktop.github.com/

## 4. 작업물 업로드
