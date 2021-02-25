# 6. MVC와 템플릿 엔진
---
> MVC : Model, View, Controller

- Model
    - 애플리케이션의 상태(Data)
    - POJO(Plain Old Java Object)로 구성
    - Java Beans
- View
    - 프리젠테이션
    - 렌더링을 담당하며, HTML을 출력
    - Thymeleaf
- Controller
    - View와 Model 사이의 인터페이스 역할

비즈니스 로직과 관련된건 Controller과 Model이 처리.

## 1. MVC, 템플릿 엔진 동작 방식
---

웹브라우저 -> URL 호출 및 파라메터 전송 -> 내장 톰켓 서버 -> (스프링 컨테이너) 파라메터를 받아와 Model에 담음 -> viewResolver에서 템플릿을 찾아서 HTML 로 변환 후 웹 브라우저로 넘김