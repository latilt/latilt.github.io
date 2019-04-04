---
title: "mac 개발환경 설정"
date: 2019-04-04 22:30:00 +0900
categories: mac development setting
---
필수 프로그램

Xcode

macOS에는 기본적으로 `gcc`,`make`와 같은 컴파일 도구가 설치되어 있지 않기 때문에 명령어 도구(Commant Line Tools)를 설치해줘야 한다.

설치
```
$ xcode-select --install
```
확인
```
$ gcc
clang: error: no input files
```
---
homebrew

brew(homebrew)는 각종 커맨드라인 프로그램을 손쉽게 설치해주는 맥용 패키지 매니저이다.

설치
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

확인
```
$ brew doctor
Your system is ready to brew.
```
---
git

macOS에 기본으로 설치되어 있지만 최신 버전이 아니므로 `brew`를 이용해서 업데이트 한다.

설치
```
$ brew install git
```
설정
```
$ git config --global user.name "Your Name"
$ git config --global user.email "you@your-domain.com"
$ git config --global core.precomposeunicode true
$ git config --global core.quotepath false
```
개인정보 설정과 한글 파일명 처리 옵션

---

MySql

널리 쓰이는 오픈소스 데이터베이스 MySql이다.

설치
```
$ brew install mysql
$ brew install mysql-client
$ brew cask install mysqlworkbench
```

brew 명령어로 손 쉽게 설정이 가능하다.
```
$ brew services start mysql

==> Tapping homebrew/services
Cloning into '/usr/local/Homebrew/Library/Taps/homebrew/homebrew-services'...
remote: Counting objects: 14, done.
remote: Compressing objects: 100% (10/10), done.
remote: Total 14 (delta 0), reused 7 (delta 0), pack-reused 0
Unpacking objects: 100% (14/14), done.
Tapped 1 command (43 files, 55.2KB).
==> Successfully started `mysql` (label: homebrew.mxcl.mysql)

# 접속
$ mysql -u root
```

root 계정 비밀번호 설정

```
$ mysql_secure_installation
......
Press y|Y for Yes, any other key for No: no
Please set the password for root here.

New password: 패스워드 입력

Re-enter new password: 패스워드 확인
.....

Remove anonymous users? (Press y|Y for Yes, any other key for No) : y
Success.

Disallow root login remotely? (Press y|Y for Yes, any other key for No) : y
Success.

Remove test database and access to it? (Press y|Y for Yes, any other key for No) : y
 - Dropping test database...
Success.

 - Removing privileges on test database...
Success.
.....

Reload privilege tables now? (Press y|Y for Yes, any other key for No) : y
Success.

All done!
```

workbench 접속 권한 세팅
```
mysql> ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '0000';
```
MySql 8.0 부터의 오류로 권한 세팅을 하지 않으면 오류가 발생한다. 다운버전을 설치하던가 권한 수정을 해준다.

---