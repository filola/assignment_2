# Asignment2
원티드x위코드 백엔드 프리온보딩 과제2
- 과제 출제 기업 정보
  - 기업명 : 프레시코드
  - [프레시코드 사이트](https://www.freshcode.me/)
  - [wanted 채용공고 링크](https://www.wanted.co.kr/wd/34118)

## Members
|이름   |Github                   |Blog|
|-------|-------------------------|--------------------|
|이태성 |[yotae07](https://github.com/yotae07)     | 추가   |
|임유선 |[YusunL](https://github.com/YusunL)   | 추가   |
|윤현묵 |[fall031-muk](https://github.com/fall031-muk) | https://velog.io/@fall031   |
|김정수 |[hollibleling](https://github.com/hollibleling) | https://velog.io/@hollibleling  |
|최현수 |[filola](https://github.com/filola) | https://velog.io/@chs_0303 |

## 과제 내용
> 아래 요구사항에 맞춰 게시판 Restfull API를 개발합니다.

### [필수 포함 사항]
- Swagger나 Postman을 이용하여 API 테스트 가능하도록 구현
- READ.ME 작성
    - 프로젝트 빌드, 자세한 실행 방법 명시
    - 구현 방법과 이유에 대한 간략한 설명
    - 완료된 시스템이 배포된 서버의 주소
    - Swagger나 Postman을 통한 API 테스트할때 필요한 상세 방법
    - 해당 과제를 진행하면서 회고 내용 블로그 포스팅

### [개발 요구사항]
- Database 는 RDBMS를 이용합니다
- 로그인 기능(JWT 인증 방식)

## 기술스택
- python, django-rest-framework
- sqlite3
- AWS EC2
- Slack, Git

## 구현 기능
### 로그인 기능
- 내용추가

### 상품 관리 기능
- 상품 전체목록 조회 가능 및 페이징 기능(한 페이지당 5개 상품)
- 사용자는 상품 조회만 가능하며 관리자는 상품 추가/수정/삭제 가능

## API 실행 방법(endpoint 호출방법)

### ENDPOINT

| Method | endpoint | Request Header | Request Body | Remark |
|:------:|-------------|-----|------|--------|
|POST|/user||email, password, role|회원가입|
|POST|/api/token/||email, password|로그인|
|POST|/product|bearer token|category, name, description, isSold, badge|상품 등록|
|GET|/product|bearer token|    |전체 상품 조회|
|GET|/product/product_id|bearer token|    |개별 상품 조회|
|PATCH|/product/product_id|bearer token|category, name, description, isSold, badge|상품 수정|
|DELETE|/product/product_id|bearer token|| 상품 삭제 |

## API 명세(request/response)

[post man 링크](https://documenter.getpostman.com/view/17228945/UVC3j7ZC#intro)


## 폴더 구조
```
.
├── README.md
├── requirements.txt
├── manage.py
├── freshcode
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings
│   ├── urls.py
│   └── wsgi.py
├── products
│   ├── migrations
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── models.py
│   ├── pagination.py
│   ├── permissions.py
│   ├── serializers.py
│   ├── tests.py
│   └── views.py
└── users
    ├── migrations
    ├── __init__.py
    ├── admin.py
    ├── apps.py
    ├── models.py
    ├── permissions.py
    ├── serializers.py
    ├── tests.py
    └── views.py

```

# Reference
이 프로젝트는 원티드x위코드 백엔드 프리온보딩 과제 일환으로 프레시코드에서 출제한 과제를 기반으로 만들었습니다.
