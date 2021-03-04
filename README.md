# 13. 스프링 DB 접근 기술
---

## 1. H2 데이터베이스 설치
---

[H2Database](https://www.h2database.com/html/main.html)

All  platform 다운로드

압축 해제 경로 -> bin

- 윈도우 : h2.bat 실행
- MacOS : chmod 755 h2.sh  ->  h2.sh 실행

실행 후 브라우저가 열리는데 만약 페이지가 안열리면 아이피를 localhost로 변경

1. 최초 실행시 JDBC URL 수정 없이 연결 버튼 클릭
2. 홈 디렉토리에 접근해보면 test.mv.db 파일 확인
3. 연결 끊기
4. JDBC URL : jdbc:h2:tcp://localhost/~/test 연결

소켓을 통해서 접근해야 여러곳에서 접근 가능

### SQL 문

```sql
drop table if exists member CASCADE;
create table member
(
    id bigint generated by default as identity,
    name varchar(255),
    primary key (id)
);
```

```sql
SELECT * FROM member;
```

```sql
insert into member(name) values('spring');
```