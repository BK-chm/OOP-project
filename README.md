# OOP-Project
# 🎮 **디지털 게임 상점 (Digital Game Store)**

Java Swing 기반의 **디지털 게임 상점 프로젝트**입니다.  
게임 구매, 찜, 리뷰, 친구 기능 등을 포함한 객체지향 프로그래밍 과제입니다.

---

## 🧩 프로젝트 개요

| 항목 | 내용 |
|------|------|
| **언어 / 환경** | Java (JDK 17 이상), Swing |
| **버전 관리** | Git + GitHub |
| **기간** | 2025.10 ~ 2025.11 |
| **인원** | 6명 |
| **브랜치 구조** | main → dev → feature/* |

---

## 📁 코드 및 데이터 구조

```bash
OOP-project/
│
├── data/
│   ├── games.txt          # 게임 목록
│   ├── users.txt          # 회원 정보
│   ├── purchase.txt       # 구매 내역
│   └── review.txt         # 리뷰 데이터
│
└── src/
    ├── util/
    │   ├── Manageable.java
    │   └── Factory.java
    │
    ├── data/
    │   ├── Game.java
    │   ├── User.java
    │   └── Review.java
    │
    ├── manager/
    │   ├── ShopManager.java
    │   ├── UserManager.java
    │   ├── PurchaseManager.java
    │   └── ReviewManager.java
    │
    └── ui/
        ├── MainFrame.java
        ├── LoginPanel.java
        ├── RegisterPanel.java
        ├── ShopPanel.java
        ├── CartPanel.java
        ├── LibraryPanel.java
        ├── WishlistPanel.java
        ├── FriendPanel.java
        └── MyPagePanel.java

main                ← 최종 안정 버전
└── dev             ← 통합 개발 브랜치
     ├── feature/user-system
     ├── feature/shop-system
     ├── feature/purchase-system
     ├── feature/review-system
     └── feature/friend-system

📦 feature/user-system

기능: 로그인, 회원가입, 마이페이지
포함 파일:

src/data/User.java  
src/manager/UserManager.java  
src/ui/LoginPanel.java  
src/ui/RegisterPanel.java  
src/ui/MyPagePanel.java

🛒 feature/shop-system

기능: 상점, 찜, 장바구니
포함 파일:

src/data/Game.java  
src/manager/ShopManager.java  
src/ui/ShopPanel.java  
src/ui/CartPanel.java  
src/ui/WishlistPanel.java

💳 feature/purchase-system

기능: 구매 및 라이브러리
포함 파일:

src/manager/PurchaseManager.java  
src/ui/LibraryPanel.java  
data/purchase.txt  

📝 feature/review-system

기능: 리뷰 작성 및 관리
포함 파일:

src/data/Review.java  
src/manager/ReviewManager.java  
data/review.txt  

👥 feature/friend-system

기능: 친구 추가 및 라이브러리 열람
포함 파일:

src/ui/FriendPanel.java  
src/data/User.java (friends 필드 추가)  
src/manager/UserManager.java (친구 기능 메서드 추가)  

## 🧭 팀원 Git 사용 가이드 (처음부터 단계별 설명)

### 🪜 1️⃣ GitHub에서 프로젝트 내려받기 (Clone)

리더가 만든 저장소 주소를 복사합니다.  
(예시)  
https://github.com/BK-chm/OOP-project.git

이제 내 컴퓨터에 저장합니다 👇  
git clone https://github.com/BK-chm/OOP-project.git
→ 이 명령을 실행하면 OOP-project 폴더가 생깁니다.
→ Visual Studio Code 또는 Eclipse에서 이 폴더를 열면 됩니다.

🌿 2️⃣ 브랜치 목록 확인하기
현재 어떤 브랜치가 있는지 확인합니다.

git branch -a
결과 예시:

* main
  dev
  remotes/origin/feature/user-system
  remotes/origin/feature/shop-system
  remotes/origin/feature/purchase-system
  remotes/origin/feature/review-system
  remotes/origin/feature/friend-system
💡 3️⃣ 본인 담당 브랜치로 이동하기
예를 들어 “리뷰 시스템”을 담당한다면 👇

git fetch origin
git checkout feature/review-system
다른 팀원 예시 👇

역할	브랜치 명령어
로그인/회원가입	git checkout feature/user-system
상점/장바구니	git checkout feature/shop-system
구매/라이브러리	git checkout feature/purchase-system
리뷰	git checkout feature/review-system
친구 기능	git checkout feature/friend-system

✏️ 4️⃣ 코드 수정 / 추가 후 저장
작업 후 변경사항을 저장합니다 👇

git add .
git commit -m "Add ReviewManager save function"
💡 commit 메시지는 영어로 짧고 명확하게 (무엇을 추가/수정했는지)

🚀 5️⃣ 브랜치에 푸시하기 (업로드)

git push origin feature/review-system
“review-system” 부분은 본인 담당 브랜치 이름으로 변경하세요.
이 명령을 실행하면 팀 공용 GitHub에 코드가 올라갑니다.

🔁 6️⃣ Pull Request(PR) 만들기
GitHub 저장소 페이지로 이동

"Pull Requests" → "New Pull Request" 클릭

base: dev ← compare: feature/본인브랜치 로 설정

제목과 내용을 간단히 입력

Create Pull Request 클릭

→ 리더가 코드 확인 후 dev로 병합합니다.

🔄 7️⃣ 최신 코드 받기 (중요!)
다른 팀원이 코드를 올린 뒤에는 꼭 dev를 최신으로 받아야 합니다 👇

git checkout dev
git pull origin dev
그리고 내 브랜치로 돌아와 최신 변경사항을 반영합니다 👇

git checkout feature/review-system
git merge dev
✅ 요약 정리
단계	명령어	설명
1️⃣	git clone <주소>	프로젝트 내려받기
2️⃣	git branch -a	브랜치 목록 확인
3️⃣	git checkout feature/기능명	본인 브랜치로 이동
4️⃣	git add . / git commit -m "메시지"	변경사항 저장
5️⃣	git push origin feature/기능명	코드 업로드
6️⃣	GitHub → PR 생성	base: dev ← compare: feature/브랜치
7️⃣	git pull origin dev / git merge dev	최신 코드 가져오기

💬 핵심 요약

✅ 새 브랜치는 만들지 않습니다.
✅ 각자 본인 담당 feature 브랜치에서만 작업합니다.
✅ 완료 후 Pull Request로 dev에 병합합니다.

📈 작업 흐름
feature/* → dev → main
