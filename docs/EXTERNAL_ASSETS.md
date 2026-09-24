---
title: EXTERNAL_ASSETS
created: 2026-09-24
---

# 외부 저장 자산 (Google Drive)

git에 넣지 않은 파일 목록. 무결성은 SHA-256으로 확인한다(전체 해시는 `00_baseline_biomni/external_assets_hashes.csv`).

| 파일 | 크기 | 원래 위치(bundle 내) | Drive 링크 |
|---|---|---|---|
| `presentation_graves_ted_landscape.pptx` (v1, 15 slide) | 654,953 B | `landscape_v1/` | TODO(업로드 후 기입) |
| `presentation_graves_ted_landscape_v2.pptx` (v2, 15 slide, canonical) | 801,792 B | `landscape_v2/` | TODO |
| `presentation_graves_ted_landscape_v2.slides/slide-001~015.png` (렌더) | 약 2.7 MB | `landscape_v2/` | TODO(pptx와 같은 폴더) |
| `worker-0.ipynb` (v1/v2 실행 trace) | 8,012,145 B | `execution_trace/` | TODO |
| `GD_TED_deck_260914.pptx` (29 slide, claude.ai Project 보관) | 미확인 | 이 폴더에 없음 | TODO(claude.ai에서 확보 필요) |

## 참고

- Drive 폴더 권장 경로: `GD_TED/decks/` (pptx), `GD_TED/traces/` (ipynb).
- 새 deck을 만들 때(JHA-86 이후)도 pptx는 Drive에 두고 이 표에 행을 추가한다.
- v2 `release_manifest_v2.csv`는 pptx와 slide PNG 경로를 포함하므로, git 사본에서는 이 파일들이 없다는 점이 정상이다(해시는 외부 자산 표로 대체 확인).
