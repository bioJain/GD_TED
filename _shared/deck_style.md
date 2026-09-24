---
title: deck_style
created: 2026-09-24
source: claude-code
---

# Deck 스타일: report-deck-style (v0.3, density high)

이 repo의 deck은 `deck_architecture_and_scoring_framework.md` 대신 **report-deck-style** 스킬 규칙을 따른다(2026-09-24 결정). 아래는 스킬 핵심의 요약이며 원본은 Claude 스킬 `report-deck-style`.

- 적용 대상: "리포트형 덱/정보형 덱/발표자 없이 단독으로 읽히는 덱". 발표용 덱은 일반 pptx 워크플로.
- 골격: Cover, Key Takeaways(최대 3장, 각 assertion에 `→ slide N` 포인터와 evidence chip), Contents, 섹션 divider, 본문, Scenarios, Catalysts, Appendix, Sources.
- 제목은 결론 문장(한국어 약 45자, 2줄 이내). "개요", "현황" 같은 topic label 금지(divider만 명사구 허용).
- 슬라이드마다 source line: `Source: <기관/저자, 문서, 날짜>. Evidence: <A-D>. As of: <날짜>.`
- Evidence grade: A 동료심사 논문/규제 문서/완료 시험 primary endpoint; B 회사 공시(미심사); C 2차 자료(KOL, DB, 뉴스); D 분석가 추론/TAM 추정. 슬라이드 footer에는 그 슬라이드의 최저 등급. D는 "Our view"/"Considerations" 박스 또는 hedged 문장에만.
- 형식: 16:9, Arial + Malgun Gothic, 본문 10.5pt, 표 9pt, 최소 8pt. 애니메이션 없음, 흑백 인쇄 가독성.
- 의견은 "Our view" 박스(1~2문장)에 격리. 추정치에는 "E" 접미.
- 가운뎃점(·) 금지. 영어 기술 용어 유지.
- QA: 스킬의 QA checklist 전 항목 통과 후 전달. 이 repo에서는 deck 개요 md를 먼저 `06_deck/`에 두고, pptx 본체는 Google Drive.

## 적용 메모

- Biomni v2의 15 slide deck은 이 스타일 이전 산출물이다(source footer는 있으나 evidence grade 체계는 다름). 새 deck(JHA-86 이후)부터 위 규칙 적용.
- Biomni v2 claim의 blind verdict(`support` 등)와 report-deck-style evidence grade(A-D)는 별개 체계다. 매핑이 필요하면 근거 tier(`evidence_tier` 컬럼)를 참조해 slide별로 명시한다.
