# TAM/SAM external source

## `SCLC_Graves_population_model.xlsx`

- Source: [Google Sheets workbook](https://docs.google.com/spreadsheets/d/1urdrkYPYPKDpIBIhP0GsPKjK62GlxgtKkq8T2hIr_gk/edit?usp=sharing)
- Direct download: [Google Drive XLSX export](https://docs.google.com/spreadsheets/d/1urdrkYPYPKDpIBIhP0GsPKjK62GlxgtKkq8T2hIr_gk/export?format=xlsx)
- Storage: external Google Drive asset only; binary is not committed to this repository
- Source review date: 2026-09-28
- Reviewed-export SHA-256: `f94ece71e0bfb19d095a49ddb9b5f8b69ff5768852b94871af1daaf1c393991d`
- Purpose: PR #19에서 검토한 외부 workbook으로 직접 연결하고, 검토 시점 export와 후속 download의 동일성을 hash로 확인.

외부 Google Sheets는 변경될 수 있으므로 현재 direct export의 hash가 위 값과 다르면 검토 이후 원본이 변경된 것으로 취급함. 이 외부 자산은 원본의 근거 품질을 상향하지 않음. `01_Assumptions`/`05_Sources`에 표시된 analyst assumption, 2차 출처, 미기재 원문 URL은 그대로 한계이며, 의사결정용 base case로 승격하기 전 별도 검증이 필요함.
