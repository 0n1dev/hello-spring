# 8. 비즈니스 요구사항 정리
---

- 데이터: ID, Name
- 기능 : 등록, 조회
- 데이터가 선정되지 않음 (시나리오)

## 일반적인 웹 애플리케이션 구조
---

- 컨트롤러 : 웹 MVC의 컨트롤러 역할
- 서비스 : 핵심 비즈니스 로직
- 도메인 : 비즈니스 도메인 객체
- 리포지토리 : 데이터베이스에 접근, 도메인 객체를 DB에 저장하고 관리

# 9. 회원 도메인과 리포지토리 만들기
---

- domain : Member 추가
- repository : MemberRepository(Interface), MemoryMemberRepository 추가