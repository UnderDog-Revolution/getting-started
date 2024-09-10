# ✨ UDR 신입부원 필수 교육 레포지토리 ✨

이 레포지토리는 UDR 신입부원이 **Git**과 **GitHub**의 기본 개념을 익히고 실습할 수 있도록 도와주는 가이드입니다. Git 설치부터 브랜치 생성, 머지까지 모든 과정이 포함되어 있습니다.

## 🚀 교육 목표
- Git 및 GitHub의 기본 개념 이해
- Git 명령어 실습을 통한 버전 관리 능력 습득
- Git Flow 전략을 활용한 체계적인 개발 프로세스 이해
- .gitignore 파일의 중요성 이해 및 활용

## 🧑‍🏫 교육 진행자
- **김석범**
- **김민지**
- **박규원**

---

## 1️⃣ Git 설치하기

### Windows
1. [Git 공식 사이트](https://git-scm.com/)에서 **Git for Windows**를 다운로드합니다.
2. 설치 프로그램을 실행하고 안내에 따라 Git을 설치합니다.
3. 설치 완료 후 명령 프롬프트(cmd)나 Git Bash를 열고 `git --version` 명령어로 설치가 완료되었는지 확인합니다.

### macOS
1. **Homebrew**를 사용하는 경우 터미널에서 다음 명령어로 설치합니다:
   ```bash
   brew install git
   ```
2. 설치가 완료되면, git --version 명령어로 설치가 완료되었는지 확인합니다.

### Linux
1. 대부분의 Linux 배포판에서는 패키지 관리자를 사용하여 Git을 설치할 수 있습니다:
   ```bash
   sudo apt-get install git
   ```
2. 설치 후 git --version 명령어로 설치가 완료되었는지 확인합니다.
   
--- 

## 2️⃣ Git 기본 명령어 사용법
### 2.1 Git 초기 설정
Git 설치 후 다음 명령어로 사용자 이름과 이메일을 설정합니다. 이 정보는 Git 커밋에 기록됩니다:
   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "your.email@example.com"
   ```
### 2.2 레포지토리 복제 (git clone)
GitHub에 있는 프로젝트를 로컬로 복제하려면 다음 명령어를 사용합니다:
   ```bash
   git clone <레포지토리 URL>
   ```
예시:
   ```bash
   git clone https://github.com/username/repository.git
   ```

---

## 3️⃣ 브랜치 관리
### 3.1 브랜치 생성 (git branch)
새로운 기능을 개발하거나 작업을 할 때는 브랜치를 생성하여 작업하는 것이 좋습니다:
   ```bash
   git branch <브랜치 이름>
   ```
예시:
   ```bash
   git branch feature/new-feature
   ```
### 3.2 브랜치 이동 (git checkout)
다른 브랜치로 이동하려면 다음 명령어를 사용합니다:
   ```bash
   git checkout <브랜치 이름>
   ```
예시:
   ```bash
   git checkout feature/new-feature
   ```
### 3.3 브랜치 생성과 동시에 이동 (git checkout -b)
브랜치를 생성하면서 동시에 해당 브랜치로 이동하려면 다음 명령어를 사용합니다:
   ```bash
   git checkout -b <브랜치 이름>
   ```
예시:
   ```bash
   git checkout -b feature/new-feature
   ```
### 3.4 브랜치 삭제 (git branch -d)
작업이 끝난 브랜치를 삭제하려면 다음 명령어를 사용합니다:
   ```bash
   git branch -d <브랜치 이름>
   ```
예시:
   ```bash
   git branch -d feature/new-feature
   ```

---

## 4️⃣ 변경사항 관리
### 4.1 파일 상태 확인 (git status)
현재 작업 중인 레포지토리의 상태를 확인하려면 다음 명령어를 사용합니다:
   ```bash
   git status
   ```
### 4.2 변경된 파일을 스테이징 (git add)
변경된 파일을 스테이징하려면 다음 명령어를 사용합니다:
   ```bash
  git add <파일 이름>
   ```
모든 파일을 스테이징하려면:
   ```bash
   git add .
   ```
### 4.3 커밋 (git commit)
스테이징된 파일을 커밋하려면 다음 명령어를 사용합니다:
   ```bash
  git commit -m "커밋 메시지"
   ```
### 4.4 리모트에 푸시 (git push)
로컬에서 작업한 내용을 원격 레포지토리로 푸시하려면 다음 명령어를 사용합니다:
   ```bash
  git push origin <브랜치 이름>
   ```
예시:
   ```bash
  git push origin feature/new-feature
   ```

---

## 5️⃣ 병합 (Merge)
### 5.1 브랜치 병합 (git merge)
다른 브랜치의 작업 내용을 현재 브랜치로 병합하려면 다음 명령어를 사용합니다:
   ```bash
  git merge <브랜치 이름>
   ```
예시:
   ```bash
   git checkout develop  # 병합할 브랜치로 이동
   git merge feature/new-feature  # feature/new-feature 브랜치의 내용을 병합
   ```

---

## 🔑 Git 관리 파일: .gitignore의 중요성
`.gitignore` 파일은 Git에서 버전 관리에 포함하지 않을 파일들을 정의하는 중요한 파일입니다. 이를 통해 민감한 정보나 불필요한 파일이 레포지토리에 포함되지 않도록 할 수 있습니다.

예시 `.gitignore`:
   ```bash
   # 환경설정 파일
   .env

   # node_modules 폴더
   node_modules/

   # 빌드 파일
   dist/

   ```

---

이제 로컬 환경에서 Git을 설치하고, 레포지토리를 관리하며, 협업하는 기본적인 과정을 익혔습니다. 추가적으로 Git Flow와 협업에 대한 내용도 학습할 예정입니다. 언제든지 질문이 있으면 교육 진행자에게 물어보세요! 😊

이 문서는 Git의 설치부터, 주요 명령어 사용법, 브랜치 관리, 병합, 그리고 `.gitignore`의 중요성까지 다루고 있습니다. 전체적인 마크다운 형식을 지키며, 신입부원들이 쉽게 따라할 수 있도록 구조화하였습니다.
