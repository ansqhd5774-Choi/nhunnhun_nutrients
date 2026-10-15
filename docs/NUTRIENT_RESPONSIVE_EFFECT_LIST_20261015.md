# 영양소 본문 반응형 효과·조합 리스트 디자인 기준

개정일: 2026-10-15

## 1. 확정 목적
영양소 글에서 변화·효능·조합·상호작용처럼 항목별 설명이 필요한 구간은 가로 카드 나열보다 **세로 리스트형 정보 카드**를 우선한다.

독자는 PC와 모바일 모두에서 `항목명 → 핵심 문장 → 설명 → 필요한 주의` 순서로 빠르게 훑을 수 있어야 한다.

## 2. 소주제별 구조를 분리한다
같은 카드 모양을 모든 소주제에 억지로 재사용하지 않는다. 정보의 성격에 따라 구조를 다르게 쓴다.

### ② 한 달 복용 후 기대되는 신체 변화와 권장 대상
- **PC부터 모바일까지 항상 1열 카드**를 사용한다.
- 대상명은 카드 상단의 큰 제목으로 두고 설명은 바로 아래에 배치한다.
- `긴 대상명 | 설명` 식의 좌우 2열 구조는 사용하지 않는다.
- 긴 한국어 대상명이 좁은 칸에서 2~4줄로 꺾이지 않도록 한다.
- 카드 왼쪽 4px 색상선과 연한 배경으로만 항목 성격을 구분한다.

### ⑤ 함께 섭취하면 좋은 영양소와 주의할 상호작용
- PC·태블릿에서는 `짧은 영양소명 + 본문` 2열 구조를 사용할 수 있다.
- 모바일 600px 이하에서는 반드시 1열로 바꿔 `영양소명 → 설명` 순서로 쌓는다.
- 본문·링크·강조 문구에는 `min-width:0`, `overflow-wrap:anywhere` 등 넘침 방지 속성을 적용한다.
- 영양소명이 길어져 좌측 칸이 답답해지면 PC에서도 1열 구조를 선택할 수 있다.

## 3. 공통 카드 기준
- 항목 간 간격은 10~12px 수준
- 카드 배경은 흰색 또는 매우 연한 톤을 사용하고, 왼쪽 4px 색상선으로 항목 성격을 구분
- 과도한 그림자·진한 전체 배경·가로 3~4열 카드 남발 금지
- 원형·pill 라벨 테두리와 별도 라벨 배경은 사용하지 않는다.
- 제목은 일반 제목형 텍스트로 표시한다.

## 4. 색상 역할
- green: 긍정 변화·실천 가능한 장점
- blue: 중립 정보·섭취 맥락
- orange: 조건·주의가 필요한 정보
- red: 중요한 위험·금기·중단 기준

색은 장식이 아니라 정보 역할 구분에만 사용한다.

## 5. 제목과 본문
- 제목은 본문보다 먼저 읽히도록 PC 기준 약 17~18px, 모바일 약 16~17px, 굵기 800 수준을 사용한다.
- 글꼴은 시스템 한글 글꼴 계열을 우선하며 `system-ui / Apple SD Gothic Neo / Noto Sans KR / Malgun Gothic` 순으로 적용한다.
- 제목 색은 카드 왼쪽 색상선의 의미와 맞춰 blue·orange·green·red 계열로 구분한다.
- 제목 뒤에 별도 배경색·둥근 외곽선·캡슐형 패딩을 두지 않는다.
- 긴 설명은 한 카드 안에서 2~4문장 이내를 기본으로 한다.
- 기존 원고에 없는 정보를 디자인을 이유로 추가하지 않는다.
- 디자인 수정 작업에서는 사실·수치·제품·조합·주의사항을 임의로 늘리거나 재작성하지 않는다.

## 6. CHECK 박스
- 실제로 별도 확인이 필요한 기존 주의 문장이 있을 때만 하단 CHECK 박스를 사용한다.
- CHECK 박스를 채우기 위해 새로운 주의정보를 만들지 않는다.
- 연한 베이지 배경 + 황금색 헤더 정도로 제한한다.

## 7. 적용 우선순위
영양소 글에서는 다음 순서로 적용한다.

1. ② 한 달 복용 후 기대되는 신체 변화와 권장 대상: **상단 제목형 1열 카드 전용**
2. ⑤ 함께 섭취하면 좋은 영양소와 주의할 상호작용: **PC 2열 / 모바일 1열 반응형 조합 카드**
3. ⑥ 결핍·과다·위험: 서로 다른 위험 항목을 비교할 필요가 있을 때 정보 성격에 맞춰 별도 구조 선택

③ 복용법과 ④ TOP7 표는 정보 성격에 맞는 표·단계형 구조를 우선하고 이 리스트를 억지로 적용하지 않는다.

## 8. 반응형 기준
```css
/* ② 전용: 모든 화면에서 1열 */
.nutrient-target-card{
  display:grid;
  grid-template-columns:1fr;
  gap:6px;
  align-items:start;
}
.nutrient-target-card h3{
  margin:0;
  font-family:system-ui,-apple-system,"Apple SD Gothic Neo","Noto Sans KR","Malgun Gothic",sans-serif;
  font-size:18px;
  font-weight:800;
  line-height:1.45;
  word-break:keep-all;
}
.nutrient-target-card p{
  min-width:0;
  margin:0;
  overflow-wrap:anywhere;
}

/* ⑤ 전용: PC 2열 */
.nutrient-pair-card{
  display:grid;
  grid-template-columns:130px minmax(0,1fr);
  gap:18px;
  align-items:start;
}
.nutrient-pair-card h3{
  margin:0;
  font-size:17px;
  font-weight:800;
  line-height:1.45;
  word-break:keep-all;
}
.nutrient-pair-card p,
.nutrient-pair-card a,
.nutrient-pair-card mark,
.nutrient-pair-card strong{
  min-width:0;
  max-width:100%;
  overflow-wrap:anywhere;
}

@media (max-width:600px){
  .nutrient-target-card h3{font-size:17px;}

  .nutrient-pair-card{
    grid-template-columns:1fr;
    gap:6px;
  }
  .nutrient-pair-card h3{font-size:17px;}
}
```

## 9. 작성 원칙
- 내용이 먼저이고 디자인은 그 내용을 더 빨리 읽게 만드는 수단이다.
- 디자인 변경 때문에 정보가 추가·삭제·왜곡되면 안 된다.
- PC에서 보기 좋고 모바일에서 읽기 불편한 구조는 사용하지 않는다.
- ②와 ⑤는 질문의 역할이 다르므로 같은 좌우 분할 구조를 강제로 공유하지 않는다.
- 같은 글 안에서도 표·리스트·CHECK 박스 등 정보 유형에 맞는 형식을 선택한다.
