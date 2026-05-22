---
slug: example
title: 글 제목을 여기에 작성하세요
description: 목록 카드와 SEO에 표시될 한 줄 요약 (100자 이내 권장)
category: 일상
date: 2026-01-01
updatedAt: 2026-02-01
published: false
---

## 섹션 제목

본문 첫 제목은 H2(`##`)부터 시작하세요.

단락 사이에 빈 줄을 하나 두면 됩니다.  
줄 끝에 공백 두 개를 넣으면 줄바꿈이 됩니다.

---

## Frontmatter 필드 안내

| 필드 | 필수 | 타입 | 설명 |
|------|------|------|------|
| `slug` | ✅ | `string` | URL 경로 키 (`/articles/slug`). 영문 소문자·숫자·하이픈만 사용 |
| `title` | ✅ | `string` | 글 제목. 페이지 상단 및 목록 카드에 표시 |
| `description` | ✅ | `string` | 한 줄 요약. 목록 카드 미리보기 및 SEO `<meta description>` |
| `category` | ✅ | `'일상' \| '등산'` | 글 분류 카테고리 |
| `date` | ✅ | `YYYY-MM-DD` | 최초 발행일 |
| `updatedAt` | ☑️ | `YYYY-MM-DD` | 마지막 수정일 (선택, 수정 시 갱신) |
| `published` | ✅ | `boolean` | `true` = 공개, `false` = 비공개 (목록·상세 모두 숨김) |

> `readTime`은 본문 내용을 기반으로 자동 계산됩니다. (한국어 500자/분, 영어 200단어/분, 코드 3초/줄)

---

## 에셋 삽입

### 사진 삽입

```markdown
앞 문단 내용...

![사진 설명 텍스트](https://static.luxtud.io/images/example/photo.jpg)
*사진 아래에 표시될 캡션 문구*

다음 문단 내용...
```

### 사진 묶음 삽입

슬라이드형은 터치 디스플레이에서 좌우 스와이프로 넘겨 볼 수 있습니다.

```markdown
<!-- image-group:slide -->
![첫 번째 사진](https://static.luxtud.io/images/example/photo-1.jpg)
![두 번째 사진](https://static.luxtud.io/images/example/photo-2.jpg)
![세 번째 사진](https://static.luxtud.io/images/example/photo-3.jpg)
<!-- /image-group -->
*사진 묶음 아래에 표시될 캡션 문구*
```

맞춤형은 본문 너비 안에서 모든 사진을 한 번에 보여줍니다.

```markdown
<!-- image-group:fit -->
![첫 번째 사진](https://static.luxtud.io/images/example/photo-1.jpg)
![두 번째 사진](https://static.luxtud.io/images/example/photo-2.jpg)
![세 번째 사진](https://static.luxtud.io/images/example/photo-3.jpg)
<!-- /image-group -->
*사진 묶음 아래에 표시될 캡션 문구*
```

![사진 설명 텍스트](https://static.luxtud.io/images/example/photo.jpg)

### GPX 삽입

```markdown
산행 기록 내용...

!gpx[종주꿈나무 백두대간 북진 15-1 (중산리-매요마을)](https://static.luxtud.io/courses/example/example.gpx)

다음 문단 내용...
```

!gpx[종주꿈나무 백두대간 북진 15-1 (중산리-매요마을)](https://static.luxtud.io/courses/example/example.gpx)

### GPX 고도 프로필 삽입

```markdown
!gpx-elevation[](https://static.luxtud.io/courses/example/example.gpx)
```

!gpx-elevation[](https://static.luxtud.io/courses/example/example.gpx)

---

## 마크다운 문법 예시

**굵게**, *기울임*, ~~취소선~~, `인라인 코드`

- 항목 하나
- 항목 둘
  - 중첩 항목

1. 순서 있는 항목
2. 두 번째 항목

> 인용문은 이렇게 작성합니다.  
> 여러 줄도 가능합니다.

```typescript
const greeting = (name: string): string => {
  return `Hello, ${name}!`
}
```

| 열 1 | 열 2 | 열 3 |
|------|------|------|
| 값 A | 값 B | 값 C |

[링크 텍스트](https://example.com)
