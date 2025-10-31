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

## 🏗 코드 및 데이터 구조

OOP-project/
│
├── data/
│ ├── games.txt # 게임 목록
│ ├── users.txt # 회원 정보
│ ├── purchase.txt # 구매 내역
│ └── review.txt # 리뷰 데이터
│
└── src/
├── util/ # 공통 유틸리티
│ ├── Manageable.java
│ └── Factory.java
│
├── data/ # 데이터 클래스
│ ├── Game.java
│ ├── User.java
│ └── Review.java
│
├── manager/ # 기능별 관리 클래스
│ ├── ShopManager.java
│ ├── UserManager.java
│ ├── PurchaseManager.java
│ └── ReviewManager.java
│
└── ui/ # Swing GUI
├── MainFrame.java
├── LoginPanel.java
├── RegisterPanel.java
├── ShopPanel.java
├── CartPanel.java
├── LibraryPanel.java
├── WishlistPanel.java
├── FriendPanel.java
└── MyPagePanel.java

yaml
코드 복사

---

## 🌿 브랜치 구조 및 포함 파일

main ← 최종 안정 버전
└── dev ← 통합 개발 브랜치
├── feature/user-system
├── feature/shop-system
├── feature/purchase-system
├── feature/review-system
└── feature/friend-system

markdown
코드 복사

### 📦 `feature/user-system`
> 로그인, 회원가입, 마이페이지 기능  
**포함 파일:**
src/data/User.java
src/manager/UserManager.java
src/ui/LoginPanel.java
src/ui/RegisterPanel.java
src/ui/MyPagePanel.java

yaml
코드 복사

---

### 🛒 `feature/shop-system`
> 상점, 찜 목록, 장바구니 기능  
**포함 파일:**
src/data/Game.java
src/manager/ShopManager.java
src/ui/ShopPanel.java
src/ui/CartPanel.java
src/ui/WishlistPanel.java

yaml
코드 복사

---

### 💳 `feature/purchase-system`
> 구매 및 라이브러리 관리  
**포함 파일:**
src/manager/PurchaseManager.java
src/ui/LibraryPanel.java
data/purchase.txt

yaml
코드 복사

---

### 📝 `feature/review-system`
> 리뷰 작성, 출력 및 관리  
**포함 파일:**
src/data/Review.java
src/manager/ReviewManager.java
data/review.txt

yaml
코드 복사

---

### 👥 `feature/friend-system`
> 친구 추가, 친구 라이브러리 열람  
**포함 파일:**
src/ui/FriendPanel.java
src/data/User.java (friends 필드 추가)
src/manager/UserManager.java (친구 기능 메서드 추가)

yaml
코드 복사

---

## ⚙ 협업 규칙

### 🔹 브랜치 생성
```bash
git checkout dev
git pull origin dev
git checkout -b feature/기능명
git push origin feature/기능명
🔹 Pull Request(PR)
방향: feature/* → dev

리더만 dev → main 병합 가능
