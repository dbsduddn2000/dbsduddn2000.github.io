# 📚 `citations_cvmi.yaml` 파라미터 설명서

이 문서는 `_data/citations_cvmi.yaml` 파일에서 사용되는 각 파라미터들의 의미와 사용 방법을 설명합니다.  
해당 파일은 논문, 출판물 등의 인용 정보를 관리하는 데 사용됩니다.  

---

## 🔑 기본 파라미터

| 파라미터 | 설명 | 예시 |
|----------|------|------|
| `id` | 인용할 출처의 고유 식별자입니다. DOI, PubMed ID, ArXiv ID 등 다양한 형식을 지원합니다. | `doi:10.1098/rsif.2017.0387` |
| `type` | 출처의 종류를 명시합니다. 표시되는 아이콘에 영향을 줍니다. | `paper`, `book`, `dataset` 등 |
| `description` | 간단한 설명을 마크다운 형식으로 작성할 수 있습니다. | `Lorem ipsum _dolor sit amet_` |
| `image` | 인용 항목에 표시할 썸네일 이미지 URL입니다. | `https://publisher.com/image.jpg` |
| `buttons` | 인용 항목 아래에 표시할 버튼 목록입니다. | 아래 참고 |
| `tags` | 인용 항목에 연결할 태그 목록입니다. | `biology`, `AI`, `big data` 등 |
| `repo` | 관련된 GitHub 저장소를 지정하면, 자동으로 태그 등을 가져올 수 있습니다. | `your-lab/some-repo` |
| `title` | 인용 항목의 제목 (Manubot 자동 생성 대신 수동 입력할 때 사용) | `Some Publication Title` |
| `authors` | 저자 목록. 마크다운 사용 가능 | `[ "**Steve McQueen**", "Lightning McQueen" ]` |
| `publisher` | 출판사 이름 (수동 입력 시) | `bioRxiv` |
| `date` | 출판일. `YYYY-MM-DD` 형식 권장 | `2021-01-01` |
| `link` | 해당 인용 항목의 링크 | `https://biorxiv.org/1234` |
| `remove` | `true`로 설정 시, 해당 인용 항목을 무시하고 출력하지 않음 | `remove: true` |

---

## 🔘 버튼 구성 (`buttons`)

`buttons`는 리스트 형태로 여러 개를 설정할 수 있으며, 아래와 같은 형식으로 사용됩니다:

```yaml
buttons:
  - type: source
    link: https://github.com/your-lab/some-repo
  - type: website
    text: My Personal Website
    link: http://some-website.com/
