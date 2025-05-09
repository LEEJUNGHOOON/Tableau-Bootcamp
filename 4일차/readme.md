
# 4일차

---

**📘 Tableau Bootcamp 4일차 학습 정리 (README)**

---

**📌 오늘의 핵심 학습 목표**

•	**시간 기반 데이터 분석**을 위한 시각화 구성

•	**테이블 계산식(Table Calculation)**의 기본 원리와 활용

•	**비율 분석, 시계열 트렌드, 하이라이트, 덤벨 차트**까지 다양한 시각화 패턴 익히기

---

**🧰 실습 데이터 다운로드**

•	[📁 도시대기 미세먼지(PM10) 데이터](https://korea-tableau-users.slack.com/files/U08D6PP1P0Q/F08NRS5US5D)

•	[📁 big-mac-raw-index + Korea_Price 데이터](https://korea-tableau-users.slack.com/files/U08D6PP1P0Q/F08PATEFXRA)

---

**✅ 4일차 퀘스트 수행 가이드**

---

**1️⃣ 월별 PM10 평균 분석 (라인 차트)**

•	**목표**: 월별 평균 미세먼지(PM10) 수치를 선으로 표현

•	**시각화 유형**: 라인 차트

**🛠️ 구성 방법**:

1.	기준년월 → 열 선반 (우클릭 → **월** 선택)

2.	PM10 → 행 선반, 집계 방식: **평균**

3.	→ 월별 평균값 확인

4.	시간의 흐름으로 연속 표현하고 싶다면 → 기준년월을 **아래쪽 “월” 옵션**으로 선택

---
<img width="1203" alt="스크린샷 2025-04-23 오후 4 01 25" src="https://github.com/user-attachments/assets/c58d296b-ecc2-4918-9e3f-72f4484a3d17" />

**2️⃣ 시도별 월별 미세먼지 변화 (하이라이트 테이블)**

•	**목표**: 월별 평균 PM10 변화량을 시도별로 시각화

•	**시각화 유형**: 하이라이트 테이블 (Heatmap)

**🛠️ 구성 방법**:

1.	열: 기준년월 (불연속형 월)

2.	행: 시도

3.	마크 유형: 사각형

4.	색상: 평균 PM10, 높을수록 붉게 / 낮을수록 파랗게 설정

---
<img width="1207" alt="스크린샷 2025-04-23 오후 4 06 38" src="https://github.com/user-attachments/assets/84718644-1696-42c9-8765-5e282e2a4061" />

**3️⃣ 빅맥 가격 변동 비율 (테이블 계산)**

•	**목표**: 2000년 대비 2020년의 빅맥 가격 상승률 비교

•	**시각화 유형**: 바 차트 + 테이블 계산

**🛠️ 구성 방법**:

1.	Date → 열 선반 → 2000년, 2020년 필터로 선택

2.	Dollar Price → 행 선반

3.	마크: 막대

4.	Dollar Price → 우클릭 → **퀵 테이블 계산 → 비율 차이**

5.	테이블 계산 편집 → 계산 기준: **Date 기준 (처음 값 기준)**

📌 **Tip**: 가격 상승률은 ((2020 - 2000)/2000)*100 식과 동일하게 작동

---
<img width="1207" alt="스크린샷 2025-04-23 오후 4 25 48" src="https://github.com/user-attachments/assets/adc3702f-2987-4eec-b0db-39c2f501bbc3" />

**4️⃣ 덤벨차트로 최소/최대 빅맥가격 변화 분석**

•	**목표**: 연도별 최소/최대 Dollar Price 및 Korea_Price의 분포와 격차 확인

•	**시각화 유형**: Dumbbell Chart (원 + 선 조합 이중축)

**🛠️ 구성 방법**:

1.	행: Date (불연속형 년월)

2.	열: 측정값

3.	필터: 측정값 이름 → Dollar Price, Korea_Price

4.	집계 방식:

•	Dollar Price → **최소값**, **최대값**으로 2번 사용

•	Korea_Price → **합계**

5.	마크: 원, 색상 → 측정값 이름

6.	열의 측정값 복사(Ctrl + Drag) → 2개의 마크 생김

7.	복사된 마크를 선으로 변경 → 색상을 경로로 이동

8.	이중축 설정 → 축 동기화 → 축 순서 변경으로 시각적 흐름 조정

---
<img width="1209" alt="스크린샷 2025-04-23 오후 4 48 01" src="https://github.com/user-attachments/assets/f6cbe4f1-4096-4ade-b11c-40635cb0113b" />

**🧠 오늘의 개념 요약**

| **개념** | **설명** |
| --- | --- |
| 라인차트 | 시간의 흐름에 따른 트렌드 분석 |
| 하이라이트 테이블 | 텍스트 기반 데이터에 색상 추가로 패턴 강조 |
| 테이블 계산식 | 기존 값 기반으로 계산된 값 생성 (비율, 누적 등) |
| 덤벨차트 | 최소/최대 값의 격차를 직관적으로 표현하는 시각화 |
| 연속형 vs 불연속형 날짜 | 연속: 연속적 축 표현 / 불연속: 범주형 표현 |

---

**🏁 마무리**

•	4일차에서는 **시간 기반 분석의 핵심 도구**인 테이블 계산과 시각적 기법을 다양하게 다뤘습니다.

•	특히 **테이블 계산식**은 실무에서 KPI 분석, 성장률 계산 등 광범위하게 활용되므로 **꼭 익혀두어야 할 핵심 기능**입니다.

•	덤벨차트는 비교 분석을 직관적으로 표현할 수 있어 **프레젠테이션용 시각화**로 강력합니다.

---
