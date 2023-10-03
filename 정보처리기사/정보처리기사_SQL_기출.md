01 테이블의 특정 행을 입력할 수 있는 DML 구문은?

​

INSERT

​

02 트랜잭션 제어 명령어 중 ‘트랜잭션 진행 중 특정 지점으로 되돌리기 위해 설정하는 명령어’는 무엇인가?

​

savepoint ( checkpoint도 정답입니다)

​

​

03 다음 보기 중 DDL 구문을 선택하시오

INSERT   CREATE   SELECT   ALTER   DROP   DELETE   UPDATE

CREATE, ALTER, DROP

​

​

[4~11]

PRIMARY KEY

FOREIGN KEY

UNIQUE

CHECK

TABLE

VIEW

INDEX

SEQUENCE

SYNONYM

DESCRIBE

CASE

DECODE

SYSDAYE

SELECT

FROM

WHERE

USER_TABLES

DISTINCT

GROUP BY

HAVING

NVL

NOT NULL

SUBSTR

ORDER BY

​

04 중복된 행을 자동으로 제거해주는 명령어(=키워드)는 무엇인가?

​

DISTINCT

​

05 테이블 또는 뷰의 구조를 조회할 때 사용하는 명령어

​

DESCRIBE

​

06 데이터 검색 시 결과를 정렬할 때 사용하는 명령어는 무엇인가?

​

ORDER BY

​

07 물리적인 테이블을 기반으로 생성되며, 데이터 딕셔너리에 SELECT 구문 형태로 저장되는 객체는 무엇인가?

​

VIEW

​

08 그룹에 제하는 조건문을 작성할 수 있는 절은 무엇인가?

​

HAVING

​

09 테이블에 NULL 값이 들어가지 못하게 막아주는 제약조건

​

NOT NULL

​

10 NOT NULL과 UNIQUE의 성격을 모두 가지고 있는 제약조건

​

PRIMARY KEY

​

11 자신의 테이블이나 다른 테이블의 특정 컬럼을 참조하는 제약조건

​

FOREIGN KEY

​

​

12 사원 테이블로부터 부서번호가 50인 사원들의 사원번호, 이름, 급여를 조회하는 '사원뷰50' 뷰(VIEW)를 생성하는 DDL 구문을 작성하시오

​

CREATE VIEW 사원뷰50

AS

(SELECT 사원번호, 이름, 급여

FROM 사원

WHERE 부서번호=50);

* 서브쿼리의 소괄호(   )는 없어도 상관없음

​

​

13 사원 테이블을 사용하여 사원의 이름과 커미션율 컬럼을 출력하되 커미션을 받지 않는 사원을 제외한 정보만 출력하는 쿼리 구문을 작성하시오. (커미션을 받지 않는 사원의 커미션 컬럼의 값은 NULL이다)

SELECT 이름, 커미션율

FROM 사원

WHERE 커미션율 IS NOT NULL;

​

14 사원2 테이블을 삭제하는 쿼리구문을 작성하시오.

DROP TABLE 사원2;​​

​

15 TITLE 테이블에 아래와 같이 데이터를 삽입하는 SQL(DML) 문장을 작성하시오. (테이블에는 아래 4개의 컬럼만 있다.)

​

테이블명

TITLE

컬럼명

TITLE_ID

TITLE

RATING

RELEASE DATE

데이터값

1

ORACLE

R

05-JUN-17

​

1)

INSERT INTO title(title_id, title, rating, release_date)

VALUES (1, 'ORACLE', 'R', '05-JUN-17');

​

2) ** 모든 컬럼에 데이터를 넣을 경우

   테이블명 뒤에 따로 컬럼명을 적지 않고, VALUES 뒤쪽에 데이터값만 컬럼의 순서대로 넣음

INSERT INTO title

VALUES (1, 'ORACLE', 'R', '05-JUN-17');

​

16 사원 테이블로부터 이름이 ‘박’으로 시작되는 사원들의 회원번호, 이름, 부서번호를 출력하는 구문을 작성하시오.

SELECT 회원번호, 이름, 부서번호

FROM 사원

WHERE 이름  LIKE '박%';

​

17 다음 빈칸에 알맞은 키워드를 넣어 쿼리 구문을 완성하시오.

SELECT 부서번호, AVG(급여) as 평균급여

FROM 사원

GROUP BY 부서번호

( HAVING ) AVG(급여) > 6000;

​

18  조건에 맞추어 SQL문을 작성하시오. 2020.2차 기출

① 학생 테이블에서 3, 4학년인 학번, 이름을 검색

② IN 함수를 사용하여 작성할 것

③ 조건에 맞지 않을 경우, 오답으로 처리됨

테이블명: 학생

학번

이름

학년

20171234

개구리

4

20183456

맹꽁이

3

20195678

두꺼비

2

SELECT 학번, 이름 FROM 학생 WHERE 학년 IN (3,4);

​

​

19. student 테이블의 name 속성에 idx_name 이름으로 인덱스로 생성하는 명령어를 작성하시오. 2020.2차 기출

CREATE INDEX idx_name ON student(name);

​

20. 사원 테이블에서 부서번호가 30, 60인 사원의 부서번호와 급여를 부서번호 기준으로 내림차순, 급여 기준으로 오름차순 정렬하여 조회하시오.

SELECT 부서번호, 급여

FROM 사원

WHERE 부서번호 IN (30,60)

ORDER BY 부서번호 DESC, 급여 (ASC);