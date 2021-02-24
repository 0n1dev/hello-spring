# 3. View 환경설정
---
## 1. Welcome Page 만들기
---
> 경로 resources/static/index.html

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
Hello
<a href="/hello">Spring</a>
</body>
</html>
```

- 스프링 부트가 제공하는 Welcom Page 기능
    - 스프링 부트는 static 경로 내에서 index.html 파일을 먼저 찾음.
    - index.html 을 못찾으면 index 템플릿을 찾음.

## 2. Thymeleaf 사용하기
---
### Thymeleaf 탬플릿 추가
> 경로 resources/templates/hello.html

```html
<!DOCTYPE html>
<html xmlns:th="http://www.thymeleaf.org">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
    <p th:text="'안녕하세요. ' + ${data}">안녕하세요. 손님 </p>
</body>
</html>
```

### HelloController 추가
> 경로 src/main/java/hello.hellospring/controller/HelloController

```java
@Controller
public class HelloController {

    @GetMapping("hello")
    public String hello(Model model) {
        model.addAttribute("data", "hello!"); // 데이터 넘김
        return "hello"; // hello를 찾아 랜더링 해라.
    }
}
```

- 컨트롤러에서 리턴 값으로 문자를 반환하면 뷰 리졸버(viewResolver)가 화면을 찾아서 처리한다.
- `resources:templates/` + {ViewName} + .html