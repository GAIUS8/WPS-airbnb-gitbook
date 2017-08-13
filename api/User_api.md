---
description: This page is Description of User API
---

- [ ] # User API

## User list

> 현재 생성되어 있는 User의 목록을 반환합니다.

**URL**  
`/apis/user/`

**Method**  
`GET`

**URL Params**

해당사항 없음

### Success Response

**HTTP Status Code**  
`200 OK`

**Content**



```json
[    
    "pk": [house primary key],
        "host": {
            "pk": [user primary key],
            "username": [suer name - email],
            "email": [email],
            "img_profile": [profile image url],
            "first_name": [first name],
            "last_name": [last name],
            "gender": [user's gender],
            "phone_num": [user's phone number],
            "birthday": [user's birth day],
            "preference_language": [user's main language],
            "preference_currency": [user's main currency],
            "living_site": [user's living site],
            "introduce": [user's self introduce],
            "last_login": [date of user's last login ],
            "date_joined": [user's joined date]
        },
    ......
]
```

## User signup

> 새로운 유저를 생성합니다.

**URL**  
`/apis/user/`

**Method**  
`POST`

**URL Params**

> Header

| Header 공백 유지 |
| :---: |



> Body

|     Key     | Description |   Type    | Require |   Default    | Restriction |
| :---------: | :---------: | :-------: | :-----: | :----------: | :---------: |
|    email    |   가입할 이메일   |   Email   |  True   |     N/A      |  Email 형식   |
|  password1  |   가입 비밀번호   | Character |  True   |     N/A      |    \*1\)    |
|  password2  |   비밀번호 확인   | Character |  True   |     N/A      |   "위와 동일"   |
| first\_name |    회원 본명    | Character |  False  |     null     |      -      |
| last\_name  |    회원 성     | Character |  False  |     null     |      -      |
|  birthday   |    회원 생일    |   Date    |  False  | "1990-01-01" |      -      |
|  agreement  | 회원 약관 동의 여부 |  Boolean  |  False  |     True     |      -      |


*1) 비밀번호 제한은 다음과 같습니다.

* 다른 개인정보와 비슷한 비밀번호 사용할 수 없습니다.
* 비밀번호는 최소 8자 이상이어야 합니다.
* 비밀번호는 일상적으로 사용 되는 비밀번호일 수 없습니다.
* 비밀번호는 전부 숫자로 할 수 없습니다.

### Success Response

**HTTP Status Code**  
`201 Created`

**Content**
```json
[
    {
        "email": [가입을 요청한 이메일 주소],
        "first_name": [입력한 회원의 이름 or null],
        "last_name": [입력한 회원의 성 or null],
        "birthday": [회원의 생일 or 1990-01-01],
        "agreement": true
    }
]
```









