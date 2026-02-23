# apps.txid.uk

앱과 웹 앱 쇼케이스 사이트.

## 구조

단일 정적 HTML 파일. 빌드 단계 없음.

- `index.html` — 메인 페이지
- `CNAME` — GitHub Pages 커스텀 도메인 설정

## 로컬 개발

브라우저에서 `index.html`을 직접 열면 됩니다.

```bash
# 또는 간단한 로컬 서버
python3 -m http.server 8000
```

## 배포

`main` 브랜치에 푸시하면 GitHub Actions가 자동으로 배포합니다.

## 앱 추가 방법

`index.html`의 `<main class="bento-grid">` 섹션에 새 카드 블록을 추가하세요.

카드 템플릿:

```html
<a href="앱_URL" target="_blank" rel="noopener noreferrer"
   class="app-card block rounded-2xl border border-border bg-surface-raised p-6 no-underline">
  <div class="flex items-start justify-between mb-4">
    <span class="text-4xl">이모지</span>
    <div class="flex gap-1.5">
      <span class="tag">태그</span>
    </div>
  </div>
  <h2 class="font-display text-xl font-semibold text-text-primary mb-2">
    앱 이름
  </h2>
  <p class="text-text-secondary text-sm leading-relaxed">
    앱 설명
  </p>
  <div class="mt-4 flex items-center text-accent text-sm font-mono">
    <span>열기 →</span>
  </div>
</a>
```

특정 카드를 크게 표시하려면 `card-featured` 클래스를 추가하세요.
