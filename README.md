<!-- markdownlint-disable-next-line -->
<div align="center">

  <!-- markdownlint-disable-next-line -->
  # Chirpy Jekyll Theme

  A minimal, responsive, and feature-rich Jekyll theme for technical writing.

  [![CI](https://img.shields.io/github/actions/workflow/status/cotes2020/jekyll-theme-chirpy/ci.yml?logo=github)][ci]&nbsp;
  [![Codacy Badge](https://img.shields.io/codacy/grade/4e556876a3c54d5e8f2d2857c4f43894?logo=codacy)][codacy]&nbsp;
  [![GitHub license](https://img.shields.io/github/license/cotes2020/jekyll-theme-chirpy?color=goldenrod)][license]&nbsp;
  [![Gem Version](https://img.shields.io/gem/v/jekyll-theme-chirpy?&logo=RubyGems&logoColor=ghostwhite&label=gem&color=orange)][gem]&nbsp;
  [![Open in Dev Containers](https://img.shields.io/badge/Dev_Containers-Open-deepskyblue?logo=linuxcontainers)][open-container]

  [**Live Demo** →][demo]

  [![Devices Mockup](https://chirpy-img.netlify.app/commons/devices-mockup.png)][demo]

</div>

## Features

- Dark Theme
- Localized UI language
- Pinned Posts on Home Page
- Hierarchical Categories
- Trending Tags
- Table of Contents
- Last Modified Date
- Syntax Highlighting
- Mathematical Expressions
- Mermaid Diagrams & Flowcharts
- Dark Mode Images
- Embed Media
- Comment Systems
- Built-in Search
- Atom Feeds
- PWA
- Web Analytics
- SEO & Performance Optimization

## Documentation

To learn how to use, develop, and upgrade the project, please refer to the [Wiki][wiki].

## 블로그 글 작성 및 업데이트 방법

### 1. bundle 명령어 안내

- **bundle install**
  - Gemfile에 명시된 루비 젬(gem)들을 설치합니다.
  - 프로젝트를 처음 클론했거나, Gemfile이 변경된 후 실행합니다.
  - 명령어:
    ```bash
    bundle install
    ```

- **bundle update**
  - Gemfile에 명시된 젬들의 버전을 최신으로 업데이트합니다.
  - 패키지 전체를 최신화하고 싶을 때 사용합니다.
  - 명령어:
    ```bash
    bundle update
    ```

- **bundle exec jekyll serve**
  - Jekyll 개발 서버를 실행하여 로컬에서 블로그를 미리 볼 수 있습니다.
  - 명령어:
    ```bash
    bundle exec jekyll serve
    ```

---

### 2. 블로그 글 작성 및 Git을 통한 업로드 과정

1. **새 글 작성**
   - `_posts` 폴더에 새로운 마크다운 파일(`YYYY-MM-DD-제목.md`)을 생성합니다.
   - 파일 상단에 YAML Front Matter(메타데이터)를 작성합니다. 예시:
     ```markdown
     ---
     title: "글 제목"
     date: YYYY-MM-DD HH:MM:SS +0900
     categories: [카테고리1, 카테고리2]
     tags: [태그1, 태그2]
     ---
     ```
   - 본문을 마크다운 형식으로 작성합니다.

2. **로컬에서 블로그 확인**
   - 터미널에서 아래 명령어로 Jekyll 서버를 실행합니다.
     ```bash
     bundle exec jekyll serve
     ```
   - 브라우저에서 `http://localhost:4000`에 접속하여 글이 정상적으로 보이는지 확인합니다.

3. **수정 및 저장**
   - 필요시 글을 수정하고 저장합니다.
   - 이미지 등 추가 리소스는 `assets/img/` 등 적절한 폴더에 저장합니다.

4. **Git을 통한 업로드**
   - 변경사항을 확인합니다.
     ```bash
     git status
     ```
   - (필요시) 변경 내용을 상세히 확인합니다.
     ```bash
     git diff
     ```
   - 변경된 파일을 스테이징합니다.
     ```bash
     git add .
     ```
   - 커밋 메시지를 작성합니다.
     ```bash
     git commit -m "블로그 글 추가: [글 제목]"
     ```
   - 원격 저장소(GitHub 등)에 푸시합니다.
     ```bash
     git push origin master
     ```

5. **배포 확인**
   - GitHub Pages 등에서 배포가 완료되면, 실제 블로그 주소에서 글이 정상적으로 보이는지 확인합니다.

## 마크다운 삽입 예시

### 1. 이미지 추가 방법
- `assets/img/` 폴더에 이미지를 저장한 후, 아래와 같이 삽입합니다.
  ```markdown
  ![이미지 설명](/assets/img/파일명.확장자)
  ```
- 크기 조절 등 스타일이 필요하면 HTML 태그 사용:
  ```html
  <img src="/assets/img/파일명.확장자" alt="이미지 설명" width="600"/>
  ```

### 2. 동영상 추가 방법
- **동영상 파일 업로드:**
  - 동영상 파일을 `assets/video/` 폴더에 저장하세요. (예: `assets/video/my-video.mp4`)
- **HTML `<video>` 태그로 삽입:**
  ```html
  <video src="/assets/video/파일명.mp4" controls width="600"></video>
  ```
- **여러 동영상 파일을 관리하려면** `assets/video/` 폴더를 만들어 사용하면 좋습니다.
- **이미지와 마찬가지로 절대경로(`/assets/video/파일명.mp4`)를 사용하세요.**
- 유튜브 등 외부 동영상:
  ```markdown
  [![동영상 설명](https://img.youtube.com/vi/유튜브ID/0.jpg)](https://www.youtube.com/watch?v=유튜브ID)
  ```

### 3. 링크 추가 방법
- 일반 링크:
  ```markdown
  [링크 설명](https://example.com)
  ```
- 새 창에서 열기 (HTML 사용):
  ```html
  <a href="https://example.com" target="_blank" rel="noopener">링크 설명</a>
  ```

### 4. HTML 웹페이지(iframe 등) 삽입 방법
- 외부 웹페이지를 내 글에 임베드하려면 iframe 사용:
  ```html
  <iframe src="https://example.com" width="800" height="400" frameborder="0" allowfullscreen></iframe>
  ```
- 주의: 일부 마크다운 렌더러나 GitHub Pages 보안 정책에 따라 iframe이 제한될 수 있습니다.

### 5. CSS와 함께 HTML 추가하는 방법
- 마크다운 파일 내에서 HTML 태그에 직접 인라인 스타일을 적용할 수 있습니다.
  ```html
  <div style="color: blue; font-weight: bold;">파란색 굵은 텍스트</div>
  ```
- 여러 요소에 스타일을 적용하려면 `<style>` 태그를 사용할 수 있습니다.
  ```html
  <style>
    .custom-box {
      background: #f0f0f0;
      border: 1px solid #ccc;
      padding: 16px;
      border-radius: 8px;
    }
    .custom-title {
      color: #007acc;
      font-size: 1.2em;
      font-weight: bold;
    }
  </style>
  <div class="custom-box">
    <span class="custom-title">커스텀 스타일 박스</span><br/>
    이 영역은 CSS가 적용된 HTML입니다.
  </div>
  ```
- 외부 CSS 파일을 불러오고 싶다면 `<link>` 태그를 사용할 수 있지만, GitHub Pages나 Chirpy 테마에서는 권장되지 않습니다. 대신 인라인 스타일이나 `<style>` 태그를 활용하세요.

#### CSS 범위(스코프) 안전하게 설정하는 방법
- `<style>` 태그로 CSS를 추가하면, 해당 규칙이 페이지 전체에 영향을 줄 수 있습니다.
- **고유한 클래스명/ID 사용**: 다른 글이나 요소와 겹치지 않도록 고유한 이름을 사용하세요.
  ```html
  <style>
    .my20240708-box { color: purple; }
  </style>
  <div class="my20240708-box">이것만 보라색</div>
  ```
- **부모-자식 선택자 활용**: 부모 요소에 고유 클래스를 주고, 그 하위에서만 스타일 적용
  ```html
  <style>
    .my-section .custom-title { color: green; }
  </style>
  <div class="my-section">
    <span class="custom-title">이것만 초록색</span>
  </div>
  ```
- **인라인 스타일 사용**: 한 요소에만 스타일이 필요하다면 style 속성 사용
  ```html
  <span style="color: orange;">이것만 주황색</span>
  ```
- **Tip**: 클래스명/ID에 날짜, 글 제목 등 고유 정보를 포함하면 충돌을 예방할 수 있습니다.


# 1. 인라인 스타일로 간단하게 꾸미기

예시:
```markdown
<div style="background: #f9f9f9; border-radius: 12px; padding: 20px; margin-bottom: 20px; box-shadow: 0 2px 8px #eee;">
  <h2 style="color: #007acc; margin-top: 0;">축구 공간을 창조하라 북터뷰</h2>
  <p style="font-size: 1.1em; color: #333;">
    [![축구의 보이지 않는 문법](https://img.youtube.com/vi/Z9d1oyO5f3U/0.jpg)](https://www.youtube.com/watch?v=Z9d1oyO5f3U)
  </p>
</div>
```

---

## 2. `<style>` 태그로 커스텀 클래스 정의

예시:
```html
<style>
  .pretty-box {
    background: #f9f9f9;
    border-radius: 12px;
    padding: 20px;
    margin-bottom: 20px;
    box-shadow: 0 2px 8px #eee;
  }
  .pretty-title {
    color: #007acc;
    margin-top: 0;
  }
  .pretty-desc {
    font-size: 1.1em;
    color: #333;
  }
</style>

<div class="pretty-box">
  <h2 class="pretty-title">축구 공간을 창조하라 북터뷰</h2>
  <p class="pretty-desc">
    [![축구의 보이지 않는 문법](https://img.youtube.com/vi/Z9d1oyO5f3U/0.jpg)](https://www.youtube.com/watch?v=Z9d1oyO5f3U)
  </p>
</div>


---

## Contributing

Contributions (_pull requests_, _issues_, and _discussions_) are what make the open-source community such an amazing place
to learn, inspire, and create. Any contributions you make are greatly appreciated.
For details, see the "[Contributing Guidelines][contribute-guide]".

## Credits

### Contributors

Thanks to [all the contributors][contributors] involved in the development of the project!

[![all-contributors](https://contrib.rocks/image?repo=cotes2020/jekyll-theme-chirpy&columns=16)][contributors]
<sub> — Made with [contrib.rocks](https://contrib.rocks)</sub>

### Third-Party Assets

This project is built on the [Jekyll][jekyllrb] ecosystem and some [great libraries][lib], and is developed using [VS Code][vscode] as well as tools provided by [JetBrains][jetbrains] under a non-commercial open-source software license.

The avatar and favicon for the project's website are from [ClipartMAX][clipartmax].

## License

This project is published under [MIT License][license].

## 블로그 마무리 작업 TODO 리스트

- [ ] **검색 최적화(SEO) 작업**
  - 메타 태그, 제목, 설명, 키워드 등 SEO 요소 점검 및 보완
  - 각 포스트별로 적절한 카테고리/태그/요약 작성
  - sitemap.xml, robots.txt 등 검색엔진 제출 파일 확인

- [ ] **이미지 업데이트**
  - 저해상도/누락 이미지 교체 및 추가
  - alt 속성(대체 텍스트) 작성으로 접근성 및 SEO 강화
  - 이미지 경로 및 파일명 일관성 점검

- [ ] **링크 업데이트**
  - 외부/내부 링크 정상 동작 여부 점검 및 수정
  - 깨진 링크, 리다이렉트 등 오류 링크 교체
  - 참고자료, 관련글 등 추가 링크 보완

- [ ] **기타 점검 사항**
  - 모바일/PC 등 다양한 환경에서 레이아웃 및 스타일 확인
  - 오타, 맞춤법, 문장 흐름 등 최종 교정
  - 불필요한 임시 파일, 테스트 포스트 삭제

## 티스토리 → Jekyll 마이그레이션 자동화 가이드

### 1. 티스토리 데이터 백업
- 티스토리 관리자 → 환경설정 → 데이터 관리 → 데이터 백업(내보내기) 기능 사용
- XML 파일로 글, 댓글, 카테고리, 태그 등 백업

### 2. XML → 마크다운(.md) 변환
- [tistory-to-markdown](https://github.com/gyuha/tistory-to-markdown) 또는 [jekyll-import](https://github.com/jekyll/jekyll-import) 등 오픈소스 도구 활용
- 변환 도구 실행 예시:
  ```bash
  # Node.js 기반 tistory-to-markdown 예시
  npx tistory-to-markdown --input tistory.xml --output ./_posts
  ```
- 각 글이 `_posts/YYYY-MM-DD-제목.md` 형식으로 변환됨
- Front Matter(제목, 날짜, 카테고리, 태그 등) 자동/수동 보완

### 3. 이미지 및 첨부파일 이동
- 티스토리 이미지/첨부파일은 별도 다운로드 필요
- [tistory-image-downloader](https://github.com/gyuha/tistory-image-downloader) 등 활용 가능
- 다운로드한 이미지는 `/assets/img/` 등으로 이동 후, 마크다운 내 이미지 경로 일괄 수정

### 4. 링크, 임베드, 스타일 등 보정
- 내부/외부 링크, 유튜브 등 임베드 코드 마크다운에 맞게 수정
- 필요시 HTML/CSS 스타일도 Jekyll에 맞게 보완

### 5. 카테고리/태그 구조 점검
- Jekyll의 `_data/categories.yml` 등으로 카테고리 구조 보완 가능
- 각 포스트의 Front Matter에 카테고리/태그가 올바르게 들어갔는지 확인

### 6. 로컬에서 미리보기 및 오류 수정
- `bundle exec jekyll serve`로 로컬 확인
- 깨진 이미지, 링크, 레이아웃 등 점검 및 수정

### 7. GitHub에 업로드 및 배포
- 정상적으로 변환된 글, 이미지, 설정 파일을 커밋/푸시
- GitHub Pages에서 정상적으로 보이는지 최종 확인

---

[gem]: https://rubygems.org/gems/jekyll-theme-chirpy
[ci]: https://github.com/cotes2020/jekyll-theme-chirpy/actions/workflows/ci.yml?query=event%3Apush+branch%3Amaster
[codacy]: https://app.codacy.com/gh/cotes2020/jekyll-theme-chirpy/dashboard?utm_source=gh&utm_medium=referral&utm_content=&utm_campaign=Badge_grade
[license]: https://github.com/cotes2020/jekyll-theme-chirpy/blob/master/LICENSE
[open-container]: https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/cotes2020/jekyll-theme-chirpy
[jekyllrb]: https://jekyllrb.com/
[clipartmax]: https://www.clipartmax.com/middle/m2i8b1m2K9Z5m2K9_ant-clipart-childrens-ant-cute/
[demo]: https://cotes2020.github.io/chirpy-demo/
[wiki]: https://github.com/cotes2020/jekyll-theme-chirpy/wiki
[contribute-guide]: https://github.com/cotes2020/jekyll-theme-chirpy/blob/master/docs/CONTRIBUTING.md
[contributors]: https://github.com/cotes2020/jekyll-theme-chirpy/graphs/contributors
[lib]: https://github.com/cotes2020/chirpy-static-assets
[vscode]: https://code.visualstudio.com/
[jetbrains]: https://www.jetbrains.com/?from=jekyll-theme-chirpy


## 블로그 마무리 작업 TODO 리스트

- [ ] **검색 최적화(SEO) 작업**
  - 메타 태그, 제목, 설명, 키워드 등 SEO 요소 점검 및 보완
  - 각 포스트별로 적절한 카테고리/태그/요약 작성
  - sitemap.xml, robots.txt 등 검색엔진 제출 파일 확인
  - **Site Verification**: 구글, 빙, 네이버 등 검색엔진 인증 코드 입력

- [ ] **웹 분석 도구 설정**
  - Google Analytics, GoatCounter, Umami, Matomo, Cloudflare, Fathom 등 ID 입력 및 활성화

- [ ] **댓글 시스템 설정**
  - giscus, utterances, disqus 등 provider 및 옵션 설정

- [ ] **대표 이미지/미리보기 이미지**
  - avatar, social_preview_image 등 지정

- [ ] **CDN 및 정적 자산 관리**
  - cdn, assets.self_host 등 필요시 활성화

- [ ] **기본 테마 모드 지정**
  - theme_mode(light/dark) 설정

- [ ] **티스토리 자료 마이그레이션**
  - 티스토리 데이터 백업(XML)
  - XML → 마크다운 변환 및 Front Matter 보완
  - 이미지/첨부파일 다운로드 및 경로 수정
  - 카테고리/태그 구조 점검
  - 내부/외부 링크, 임베드, 스타일 보정
  - 로컬 미리보기 및 오류 수정
  - GitHub 업로드 및 배포

- [ ] **이미지/링크/첨부파일 업데이트**
  - 저해상도/누락 이미지 교체 및 추가
  - alt 속성(대체 텍스트) 작성
  - 이미지/링크 경로 및 파일명 일관성 점검

- [ ] **기타 점검 사항**
  - 모바일/PC 등 다양한 환경에서 레이아웃 및 스타일 확인
  - 오타, 맞춤법, 문장 흐름 등 최종 교정
  - 불필요한 임시 파일, 테스트 포스트 삭제