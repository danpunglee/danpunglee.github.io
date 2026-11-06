# SLIMON (슬리몬)

위고비·마운자로 같은 GLP-1 다이어트 주사를 맞는 사람을 위한 토스 인앱(앱인토스) 미니앱입니다. 주사 기록부터 감량 그래프까지 한 화면에서 간단하게 관리합니다.

<div class="shots">
  <img src="img/slimon-home.jpg" alt="SLIMON 홈 화면 — 다음 주사 D-day, 체중, 약물 농도 그래프" loading="lazy">
  <img src="img/slimon-injections.jpg" alt="SLIMON 주사 기록 화면" loading="lazy">
  <img src="img/slimon-weight.jpg" alt="SLIMON 체중 그래프 화면" loading="lazy">
</div>

## 주요 기능 {#features}

| 기능 | 설명 |
| --- | --- |
| 💉 주사 기록 | 약 종류·용량·일시·부위·부작용 기록, 다음 주사일 D-day |
| ⚖️ 체중 그래프 | 날짜별 체중, 목표선, 목표 달성률, 주사 1회당 평균 감량 |
| 📈 약물 농도 그래프 | 반감기 기반 체내 농도 추정 곡선 (참고용) |
| 🥗 식단·식욕 메모 | 하루 식욕(1~5)과 먹은 음식, 식욕 변화 그래프 |

지원 약: 위고비(세마글루타이드), 마운자로(터제파타이드), 삭센다(리라글루타이드), 기타 직접 입력

## 기술 스택 {#stack}

- 앱인토스 WebView (`@apps-in-toss/web-framework`)
- React + TypeScript + Vite
- TDS Mobile (토스 디자인 시스템)

## 링크 {#links}

- [앱인토스 개발자 문서](https://developers-apps-in-toss.toss.im/)
- 소스 코드: 비공개 저장소 (`danpunglee/slimon`)

:::warning 안내
SLIMON은 기록·정보 제공용 서비스이며 진단·처방 등 의료 행위를 하지 않습니다. 약 사용은 반드시 의료진과 상담하세요.
:::
