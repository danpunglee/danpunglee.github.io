# 사이트 운영

이 홈페이지를 고치고 다시 배포하는 방법입니다. 별도 빌드 도구 없이 GitHub 웹 화면만으로 수정할 수 있습니다.

## 구성 {#structure}

| 항목 | 위치 |
| --- | --- |
| 주소 | `https://danpunglee.github.io` |
| 저장소 | [danpunglee/danpunglee.github.io](https://github.com/danpunglee/danpunglee.github.io) |
| 글 | `docs/*.md` (페이지 하나당 파일 하나) |
| 메뉴 순서 | `docs/sidebar.json` |
| 디자인 | `style.css` |
| 화면 동작 | `index.html` |
| 비용 | 무료 (공개 저장소 + GitHub Pages) |

## 글 수정하기 {#edit}

1. 각 페이지 맨 아래 **이 페이지 수정하기**를 누르거나, 저장소 `docs` 폴더에서 원하는 `.md` 파일을 엽니다.
2. 연필 아이콘(Edit)을 누르고 마크다운으로 내용을 고칩니다.
3. **Commit changes**를 누르면 1~2분 뒤 사이트에 반영됩니다.

## 새 페이지 추가 {#new-page}

1. `docs` 폴더에서 **Add file → Create new file**로 새 파일을 만듭니다. 예: `my-note.md`
2. 첫 줄에 `# 제목`을 쓰고, 그 아래에 본문을 씁니다.
3. `docs/sidebar.json`에서 원하는 그룹의 `items`에 한 줄을 추가합니다.

```json
{ "id": "my-note", "title": "메뉴에 보일 이름" }
```

`id`는 파일 이름에서 `.md`를 뺀 것입니다. 새 페이지 주소는 `#/docs/my-note`가 되고, 사이드바·검색·이전/다음 버튼이 자동으로 연결됩니다.

:::note 그룹 추가
`sidebar.json`에 `{ "label": "그룹 이름", "items": [ ... ] }` 블록을 추가하면 사이드바에 새 그룹이 생깁니다. 항목 사이 쉼표(`,`)를 빠뜨리지 않도록 주의하세요.
:::

## 마크다운 문법 {#syntax}

제목(`#`, `##`, `###`), 목록, 표, 링크, **굵게**, `코드`, 코드 블록 등 일반 마크다운을 그대로 쓸 수 있습니다. 여기에 두 가지가 더 있습니다.

### 안내 박스 {#admonition}

```md
:::info 제목
내용을 여기에 씁니다.
:::
```

`note`, `tip`, `info`, `warning` 네 종류가 있습니다. 제목을 생략하면 종류 이름이 표시됩니다.

### 목차 링크 이름 {#heading-id}

`## 구성 {#structure}`처럼 제목 끝에 `{#이름}`을 붙이면 오른쪽 목차의 링크 이름이 고정됩니다. 생략하면 제목 글자로 자동 생성됩니다.

## 디자인 수정하기 {#design}

색상, 글꼴, 여백 같은 디자인은 [`style.css`](https://github.com/danpunglee/danpunglee.github.io/edit/main/style.css)에 모여 있습니다. 파일 맨 위 `:root`의 변수(예: `--link`, `--btn-bg`)만 바꿔도 사이트 전체에 적용되고, 다크 모드 색은 바로 아래 `[data-theme="dark"]`에서 바꿉니다.

## 주소를 바꿀 때 {#name-change}

Organization 이름을 바꾸면 사이트 주소도 함께 바뀝니다. 이때 저장소 이름도 `새이름.github.io`로 맞춰 주어야 합니다.

:::warning 주의
공개 저장소이므로 비밀번호, 개인 연락처, 회사 내부 정보는 올리지 마세요.
:::
