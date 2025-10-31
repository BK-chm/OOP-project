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
🌿 브랜치 구조 및 담당 파일
bash
코드 복사
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

bash
코드 복사
src/data/User.java  
src/manager/UserManager.java  
src/ui/LoginPanel.java  
src/ui/RegisterPanel.java  
src/ui/MyPagePanel.java  
🛒 feature/shop-system
기능: 상점, 찜, 장바구니
포함 파일:

bash
코드 복사
src/data/Game.java  
src/manager/ShopManager.java  
src/ui/ShopPanel.java  
src/ui/CartPanel.java  
src/ui/WishlistPanel.java  
💳 feature/purchase-system
기능: 구매 및 라이브러리
포함 파일:

bash
코드 복사
src/manager/PurchaseManager.java  
src/ui/LibraryPanel.java  
data/purchase.txt  
📝 feature/review-system
기능: 리뷰 작성 및 관리
포함 파일:

bash
코드 복사
src/data/Review.java  
src/manager/ReviewManager.java  
data/review.txt  
👥 feature/friend-system
기능: 친구 추가 및 라이브러리 열람
포함 파일:

bash
코드 복사
src/ui/FriendPanel.java  
src/data/User.java (friends 필드 추가)  
src/manager/UserManager.java (친구 기능 메서드 추가)  
⚙ 협업 규칙 (팀원용)
1️⃣ 원격 브랜치 가져오기
리더가 만든 feature 브랜치를 로컬로 복사합니다.

bash
코드 복사
git fetch origin
git checkout feature/브랜치명
예시:

bash
코드 복사
git checkout feature/shop-system
2️⃣ 개발 후 커밋 & 푸시
bash
코드 복사
git add .
git commit -m "Add ShopPanel and CartPanel basic UI"
git push origin feature/shop-system
3️⃣ Pull Request(PR) 생성
GitHub 저장소 접속

New Pull Request 클릭

base: dev ← compare: feature/본인브랜치 선택

설명 작성 후 Create Pull Request

🧾 커밋 메시지 예시
예시	설명
Add UserManager and LoginPanel	기능 추가
Fix ShopPanel price filter bug	버그 수정
Update LibraryPanel layout	UI 개선
Refactor ReviewManager save logic	코드 리팩토링

✅ 요약
각 팀원은 본인 담당 feature 브랜치를 로컬로 가져와 개발합니다.
새 브랜치는 만들지 않고, 기존 브랜치에 커밋 후 PR → dev 병합 순서로 진행합니다.

🔁 작업 흐름
feature/* → dev → main

main은 항상 최종 안정 버전으로 유지합니다.
