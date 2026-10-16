# 6. Templates/ — 노트 템플릿

## 목적과 역할
반복해서 만드는 노트 유형의 **틀**을 보관합니다. Obsidian 핵심 플러그인 "템플릿"이 이 폴더를 참조하도록 설정해 사용합니다.

## 들어가는 노트
노트 유형별 템플릿 하나씩. 각 폴더의 CLAUDE.md에 정의된 frontmatter 규칙과 일치해야 합니다.
- `TPL - Fleeting.md` → `5. Zettelkasten/00. Inbox/`
- `TPL - Literature.md` → `5. Zettelkasten/10. Literature/`
- `TPL - Permanent.md` → `5. Zettelkasten/20. Permanent/`
- `TPL - MOC.md` → `5. Zettelkasten/20. Permanent/`
- `TPL - Project.md` → `1. Projects/`
- `TPL - Area.md` → `2. Areas/`
- `TPL - Resource.md` → `3. Resources/`
- `TPL - Daily.md` (일일 노트 사용 시)

## 작업 방식과 규칙
- 파일명은 `TPL - 유형.md` 형식으로 통일합니다.
- 날짜·제목은 Obsidian 템플릿 변수를 사용합니다: `{{date:YYYY-MM-DD}}`, `{{title}}`, `{{time}}`
- 템플릿은 실제 노트가 아니므로 다른 노트에서 링크하지 않습니다.
- 다른 폴더의 frontmatter 규칙을 바꾸면 해당 템플릿도 함께 수정합니다(반대도 마찬가지).
