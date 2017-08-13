## User object

| Attribute | Descriptions | Type | Require | Default | Restriction |
| :---: | :---: | :---: | :---: | :---: | :---: |
| pk | primary key | Interger | True | N/A | Auto Define |
| username | 유저 식별 ID | Email | True | N/A | Auto Define |
| email | E-mail주소 | Email | True | N/A | - |
| img\_profile | 프로필 이미지 | Image | False | null | less than 20MB |
| first\_name | 이름 | Character | False | None | - |
| last\_name | 이름의 성 | Character | False | None | - |
| gender | 성별 | Choice | False | "OTHER" | \*1\) |
| phone\_num | 전화번호 | Character | False | null | 글자수 20자 제한 |
| birthday | 생일 | DateTime | False | null | 글자수 20자 제한 |
| preference\_language | 선호하는 언어 | Character | False | null | 글자수 20자 제한 |
| preference\_currency | 선호하는 통화 | Character | False | null | 글자수 20자 제한 |
| living\_site | 사는 지역 | Character | False | null | 글자수 100자 제한 |
| introduce | 자기 소개 | Text | False | null | 글자수 300자 제 |
| last\_login | 마지막 로그인 시간 | DateTime | False | null | Auto Define |
| date\_joined | 가입 날 | DateTime | False | N/A | Auto Define |

\*1\) You can input only one of "**OTHER**" or "**MALE**" or "**FEMALE**"

