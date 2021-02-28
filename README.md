# 11. 스프링 빈과 의존관계
---

## 2. 자바 코드로 직접 스프링 빈 등록하기
---

### DI의 세가지 방법

- 생성자 주입 (추천)
```java
    private final MemberService memberService;

    @Autowired
    public MemberController(MemberService memberService) {
        this.memberService = memberService;
    }
```
- 필드 주입 (비추)
```java
    @Autowired private MemberService memberService;
```
- setter 주입 (비추)
```java
    private MemberService memberService;

    @Autowired
    public void setMemberService(MemberService memberService) {
        this.memberService = memberService;
    }
```