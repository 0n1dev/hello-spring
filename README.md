# 1. 프로젝트 생성
---
## 1. 개발 환경
---
- Java 11
- IntelliJ IDEA

## 2. [스프링 부트 스타트](https://start.spring.io/)
---
- 스프링에서 운영중인 스프링 부트 만들어주는 페이지
- Project
    - Maven
    - Gradle (추천)
- Language
    - Java
- Spring Boot
    - 스프링 부트 버전
- Project Metadata
    - Group : 기업 명
    - Artifact : 결과물
    - Name
    - Description
- Dependencies (의존성)
    - Spring Web
    - Thymeleaf (HTML 템플릿 엔진)

GENERATE 클릭 → IntlliJ 실행 → 해당 디렉토리에서 build.gradle 선택 후 Open

## 3. 프로젝트 구조
---
- .idea : IntlliJ 설정 파일
- .gradle : Gradle 폴더
- src
    - main
        - java : 패키지와 소스 파일
        - resources : java 코드 파일을 제외한 xml, html 등
- test : 테스트 관련 코드
- build.gradle : Gradle 관련 설정 파일

## 4. 프로젝트 실행
---
src → java → hello.hellospring → HelloSpringApplication → 실행 → [localhost:8080](http://localhost:8080) 접속