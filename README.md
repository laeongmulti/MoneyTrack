# 🐰💰 MoneyTrack
## KB IT's Your Life 6기 13회차 스켈레톤 프로젝트 4조

**MoneyTrack**은 매일의 수입과 지출을 손쉽게 기록하고, **시각화된 통계**를 통해 소비 습관을 파악할 수 있는 웹 기반 가계부 서비스**입니다.
<br><br/>

---

## 📌 주요 기능

- **소비 기록**  
  날짜별 수입/지출 내역을 입력하고 관리할 수 있어요.

- **통계 시각화**  
  카테고리별, 기간별로 소비 패턴을 그래프 형태로 확인할 수 있어요.

- **회원 기능**  
  로그인/회원가입 기능을 통해 개인별 기록을 관리할 수 있어요.

- **반응형 UI**  
  PC, 태블릿, 모바일 모두에서 최적화된 화면을 제공합니다.

- **커스텀 알림 & 확인창**  
  사용자에게 더 직관적인 피드백을 주기 위한 커스텀 Alert, Confirm 컴포넌트를 제공합니다.

---

## 🛠️ 사용 기술

| 분야         | 사용 스택                          |
|--------------|------------------------------------|
| **Frontend** | Vue 3, Pinia, Vue Router, Axios   |
| **Design**   | Figma (UI 디자인), Notion (기획서 작성) |
| **Server**   | JSON Server (Mock API)            |

---

## 🧑‍🤝‍🧑 팀원 소개

| **남민주**<br/>[@namminju](https://github.com/namminju) | **이가연**<br/>[@Gayeon07](https://github.com/Gayeon07) | **임창진**<br/>[@Heboen](https://github.com/Heboen) | **최혜림**<br/>[@BaileyChoi](https://github.com/BaileyChoi) | **황병권**<br/>[@laeongmulti](https://github.com/laeongmulti) 
|:---:|:---:|:---:|:---:|:---:|


---

## 📖 기획 문서
👉 [MoneyTrack Notion](https://www.notion.so/Money-Track-1d18b640ebf88016b814ce22e511f960?pvs=4)
<br></br>
(프로젝트 개요 / 기능 정의 / UI 디자인 / 기술 명세  / 브랜치 전략 / 테스트 / 프로젝트 후기 )

---

## 📸 시연 이미지
추후에 추가 예정

---

# ⚙️ 설치 방법 (Getting Started)
로컬 환경에서 이 프로젝트를 실행하는 방법은 다음과 같습니다.

### 1. 저장소 클론
```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

### 2. 패키지 설치
```bash
npm install
```

### 3. 개발 서버 실행
```bash
npm run dev
```
실행 후 브라우저에서 http://localhost:5173 으로 접속합니다.

### 4. json-server 실행 (Mock Backend)
```bash
npm install -g json-server
json-server --watch db/db.json --port 3001


