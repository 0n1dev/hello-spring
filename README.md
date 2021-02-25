# 7. API
---
## 1. @ResponseBody 사용 원리
---

웹브라우저 -> URL 호출 및 파라메터 전송 -> 내장 톰켓 서버 -> (스프링 컨테이너) @ResponseBody가 붙어 있으면 HttpMessageConverter로 넘김 -> http 응답에 바로 넘김 (객체가 오면 기본 JSON 포맷으로 반환)

- 기본 문자처리 : StringHttpMessageConverter
- 기본 객체처리 : MappingJackson2HttpMessageConverter