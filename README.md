# haeumkorean.me 새 주소 안내

예전 도메인 <https://haeumkorean.me/>에서 보여 주는 정적 안내 페이지입니다.

- 본 사이트: <https://haeum.haeonkorean.com/>
- 어휘 학습: <https://words.haeonkorean.com/>
- 자동 이동, meta refresh, JavaScript, 외부 폰트는 사용하지 않습니다. 방문자가 링크를 선택해 이동합니다.
- `rel=canonical`은 본 사이트 주소를 알려 주는 메타데이터이며 브라우저를 이동시키지 않습니다.

## 배포

전용 저장소는 `Jasujung99/haeumkorean-me`입니다. GitHub Pages에서 `main` 브랜치의 루트(`/`)를 배포하고 Custom domain을 `haeumkorean.me`로 설정합니다. 인증서 준비 후 Enforce HTTPS를 활성화합니다.

이 저장소는 로컬 `haumkorean-website/legacy-domain`의 안내 파일을 복사해 시작했습니다. 본 사이트 저장소 `Jasujung99/Jasujung99.github.io`의 코드·PR #4·Actions·Pages 설정과 독립적으로 배포합니다.

## 파일과 주소 동작

- `index.html`: 안내 페이지와 새 주소 링크.
- `404.html`: `index.html`과 같은 내용. `/education-exam`처럼 존재하지 않는 경로에서도 안내를 표시합니다. 이 경우 HTTP 상태는 정상적인 404입니다.
- `/#/education-exam` 같은 해시 주소는 서버에 `/`로 요청되므로 `index.html`이 표시됩니다.
- `CNAME`: `haeumkorean.me`.
- `favicon.svg`: 기존 해움 파비콘.
- `.nojekyll`: Jekyll 처리 비활성화.

문구를 바꿀 때는 `index.html`과 `404.html`을 함께 수정합니다. 두 HTML 파일의 내용을 동일하게 유지하세요.

## DNS

apex `haeumkorean.me`의 기존 A 레코드 4개를 유지합니다.

```text
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

기존 `www.haeumkorean.me`는 `haeumkorean.me`를 가리킵니다. 이번 배포에서는 DNS 레코드를 변경하지 않습니다. `haeum.haeonkorean.com`의 배포 설정과 DNS도 변경하지 않습니다.

[GitHub Pages 사용자 도메인 공식 안내](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site)
