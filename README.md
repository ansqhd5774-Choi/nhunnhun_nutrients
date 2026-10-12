# 한입 건강 — 영양소 프로젝트

이 저장소는 nhunnhun.tistory.com의 영양소 카테고리 전용 원고 및 프로젝트 지침을 보관합니다.

- 프로젝트 지침: [PROJECT_INSTRUCTIONS.txt](PROJECT_INSTRUCTIONS.txt)
- 공통 발행 러너: [nhunnhun_blog](https://github.com/ansqhd5774-Choi/nhunnhun_blog)

## 저장 직전 작성 검토

영양소 글은 `PROJECT_INSTRUCTIONS.txt`의 6개 소주제와 문체·검토 기준을 따른다. 저장 직전에는 도입·효능·궁합·FAQ·핵심 정리의 부정·반박·근거 한계 문장을 다시 확인한다. 같은 한계나 반박을 반복해 글의 중심으로 만들지 않고, 확인된 특징·작용·수치·섭취·선택 행동을 먼저 설명한다. 실제 과다섭취·알레르기·금기·상호작용·응급 행동 같은 안전정보는 유지한다. 일반적인 근거 한계는 강한 강조의 핵심으로 사용하지 않는다.

기존 원고의 `imageReview`를 재사용할 때 `src`, `alt`, `role`, `composition`, `sourcePage`, `author`, `license` 같은 이미지·귀속 정보는 재사용할 수 있지만 `visualChecked` 관찰값은 새 source로 복사하지 않는다. 현재 source에서 이미지 원본을 실제로 다시 확인한 경우에만 `visualChecked:true`를 새로 기록한다. 미확인 상태는 키를 생략하거나 false로 둘 수 있으며 이 값 자체를 발행 필수 게이트로 사용하지 않는다.

실제 시각 점검에서 대표 이미지로 부적합하다고 확인된 원출처는 다시 hero로 선택하지 않는다. 공통 러너의 `publishing/rejected-hero-sources.mjs`에 등록된 원출처는 direct preflight에서 `E_IMAGE_HERO_REJECTED`로 차단된다. 이 목록은 실제로 확인된 재발 사례를 수동으로 막기 위한 것이며 이미지 의미를 자동 판정하는 기능이 아니다. 대표 이미지로 부적합해도 본문 보조 이미지로 쓸 수 있는지는 별도로 판단한다.

이 검토는 자동 의미 판정이나 자동 재작성으로 대체하지 않는다. 공통 러너의 preflight는 구조·강조·이미지 등 결정적 검사를 담당하고, 작성자는 의미·문체 검토를 저장 전에 완료한다.

이 저장소에 원고를 저장하는 것만으로 Tistory Actions가 시작되지는 않습니다. 실제 제출 전 공통 발행 러너가 동일 원고를 접수했는지 확인하고, 해당 저장소의 workflow 결과와 공개 검증을 별도로 확인합니다.
