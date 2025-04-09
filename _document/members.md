## 👥 팀 멤버 설정 (파일: `_members/`)

팀 멤버를 추가하거나 제거하려면 `_members` 폴더에 Markdown 파일을 생성하거나 삭제하면 됩니다.  
예: `윤영우.md` → `/members/윤영우` 경로의 개인 페이지가 자동 생성됩니다.

---

### 📌 팀 멤버 파라미터 설명

| 파라미터        | 설명                                                                                          | 비고                                 |
|------------------|-----------------------------------------------------------------------------------------------|--------------------------------------|
| `name`           | 팀 멤버의 표시 이름입니다.                                                                    | ✅ 필수                                 |
| `image`          | 팀 멤버의 사진 URL입니다 (`/images/team/` 경로에 저장 권장).                                  | 선택                                 |
| `role`           | 조직 내 팀 멤버의 역할을 의미하며, 아이콘 및 기본 설명에 영향을 줍니다.                       | `/_data/types.yaml` 참고 가능         |
| `description`    | 멤버의 역할에 대한 구체적인 설명. `role`의 기본 설명을 덮어씁니다.                             | 선택                                 |
| `aliases`        | 논문 검색 등에서 사용할 이름의 변형(별칭) 목록입니다.                                          | 리스트 형태                          |
| `links`          | 개인 홈페이지, 이메일, 트위터 등의 소셜 링크 목록입니다.                                       | 접두사 없이 입력 (예: `twitter: user`) |

> 🧠 `role`은 고수준 분류(예: 교수, 대학원생 등)에 사용하고,  
> `description`은 각 멤버에 특화된 설명으로 사용하는 것이 기본 구조입니다.

---

### ✅ 팀 멤버 예시 파일 (`윤영우.md`)

```markdown
---
name: 윤영우
image: images/team/yyw.jpg
role: programmer
description: Senior Programmer
aliases:
  - T Member
  - T. Member
links:
  home-page: https://yyw-website.com/
  email: yyw-member@email.com
  twitter: yyw_twitter
---

윤영우에 대한 소개글 ~~~~
