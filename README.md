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
├── util/
│ ├── Manageable.java
│ └── Factory.java
│
├── data/
│ ├── Game.java
│ ├── User.java
│ └── Review.java
│
├── manager/
│ ├── ShopManager.java
│ ├── UserManager.java
│ ├── PurchaseManager.java
│ └── ReviewManager.java
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

---

## 🌿 브랜치 구조 및 담당 기능

main ← 최종 안정 버전
└── dev ← 통합 개발 브랜치
├── feature/user-system ← 로그인 / 회원가입 / 마이페이지
├── feature/shop-system ← 상점 / 찜 / 장바구니
├── feature/purchase-system ← 구매 / 라이브러리
├── feature/review-system ← 리뷰 작성 / 출력
└── feature/friend-system ← 친구 기능

| 브랜치 | 담당 기능 | 주요 파일 |
|--------|------------|------------|
| `feature/user-system` | 로그인, 회원가입, 마이페이지 
`User.java`, 
`UserManager.java`, 
`LoginPanel.java`, 
`RegisterPanel.java`, 
`MyPagePanel.java` 
|
| `feature/shop-system` | 상점, 찜, 장바구니 
`Game.java`, 
`ShopManager.java`, 
`ShopPanel.java`, 
`CartPanel.java`, 
`WishlistPanel.java` 
|
| `feature/purchase-system` | 구매 및 라이브러리 
`PurchaseManager.java`, 
`LibraryPanel.java`, 
`purchase.txt` 
|
| `feature/review-system` | 리뷰 작성 및 관리 
`Review.java`, 
`ReviewManager.java`, 
`review.txt` 
|
| `feature/friend-system` | 친구 추가, 라이브러리 열람 
`FriendPanel.java`, 
`User.java(friends 필드)`, 
`UserManager.java(친구 기능 추가)` 
|

---

## ⚙ 팀원 협업 규칙 (브랜치 생성 X, 가져오기 O)

### 🔹 1️⃣ 원격 브랜치 가져오기
> 리더가 만들어둔 feature 브랜치를 로컬에 복사하는 과정입니다.

```bash
# 최신 브랜치 정보 가져오기
git fetch origin

# 본인이 담당할 브랜치로 이동 (예: 리뷰 담당자)
git checkout feature/review-system
🔹 2️⃣ 로컬에서 개발 후 커밋 & 푸시
bash
코드 복사
git add .
git commit -m "Add ReviewManager logic"
git push origin feature/review-system
🔹 3️⃣ Pull Request (PR) 생성
GitHub 저장소 접속

New Pull Request 클릭

base: dev ← compare: feature/본인브랜치

설명 작성 후 Create Pull Request

리더가 dev로 병합 후 테스트 완료 시 main에 최종 반영됩니다.

