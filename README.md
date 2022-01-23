# MYSQL

- https://www.w3schools.com/mysql/trymysql.asp?filename=trysql_select_all

### SELECT

###  '--' : 주석

### 'SELECT "원하는 정보" FROM "TABLE"'

### '*' : 모든 것을 가져온다.

### 'WHERE' : 구문 뒤 조건을 붙여 원하는 데이터 가져온다. (ROW);
- EX) SELECT * FROM Orders
      WHERE EmployeeID = 3 ;

### ORDER BY : 구문을 이용해 특정 column 기준으로 데이터 정렬 (ASC: 오름차순, DESC : 내림차순)
- EX) SELECT * FROM OrderDetails
      ORDER BY ProductID ASC, Quantity DESC;

### LIMIT: QUANTITY OR SKIP, QUANTITY 원하는 위치에서 원하는 만큼의 데이터를 가져온다.
- EX) SELECT * FROM Customers
      LIMIT 10;
- EX) SELECT * FROM Customers
      LIMIT 20, 10;

### AS(ALIAS) : COLUMN 명을 변경
- EX) SELECT CustomerID AS ID FROM Customers; 

### TRUE, FALSE : MYSQL에서는 TRUE = 1 , FALSE =0 로 저장

### GROUP BY : 조건에 따라 집계된 값을 가져온다.
- WITH ROLLUP: 전체 집계값
- HAVING : 그룹화된 데이터 걸러내기 (WHERE은 GROUP BY전, HAVING은 GROUP BY후)
- DISTINCT : 중복된 값을 제거

### JOIN : 양쪽 모두 값이 있는 행(NOT NULL) 반환
- LEFT/RIGHT JOIN: 반대쪽에 데이터가 있든 없든, 선택된 방향에 있으면 출력 - 행 수 결정
- CROSS JOIN : 조건없이 모든 조합 반환

### UNION : 중복을 제거한 집합 
- UNION ALL : 중복을 제거하지 않은 집합



|    연산자      |          의미             |
| :--------------|--------------------------| 
| ' +,-,*,/'     | 더하기,빼기,곱하기,나누기  |
|  '% , MOD'     |        나머지             |
|     IS         | 양쪽이 모두 TRUE OR FALSE |
|   IS NOT       | 한쪽은 TRUE, 한쪽은 FALSE |
|  AND , &&      |  양쪽이 TRUE일 떄 TRUE    |
|   OR , ||      |  한쪽은 TRUE 면 TRUE      |
|      =         |     양쪽 값이 같음        |
|   != , <>      |     양쪽 값이 다름        |
|    > , <       |     값이 더 큼            |
|BETWEEN A AND B |  두 값 사이에 있음         |
|NOT BETWEEN AND |  두 값 사이가 아닌 곳      |
|   IN(...)      |   괄호 안의 값 안에 있음   |
|  NOT IN (...)  |  괄호 안의 값들 안에 없음  |
|  LIKE '...%...'|  0-N 개의 문자를 가진 패턴 |
|  LIKE '..._...'| _개만큼의 문자를 가진 패턴 | 
|   ROUND        |         반올림            |
|   CEIL         |           올림            |
|   FLOOR        |           버림            |
|   ABS          |         절대값            |
|  GREATEST()    |   ( ) 안에서 가장 큰 값    |
|   LEAST()      |   ( ) 안에서 가장 작은 값  |
|    MAX         |      가장 큰 값           |
|    MIN         |      가장 작은 값         |
|   COUNT()      |        수량(NULL 제외)    |
|    SUM         |         총 합             |
|    AVG         |         평 균             |
|   POW(A,B)     |        A를 B 만큼 제곱     |
|   SQRT         |       제곱근              |
|  TRUNCATE(N,n) |   N을 소숫점 n자리까지 선택 |
| UPPER,UCASE    |        대문자             |
| LOWER,LCASE    |        소문자             |
|  CONCAT()      |     () 안의 내용을 이어붙임|
|CONCAT_WS(S,..) |   ()안의 내용 S로 이어 붙임|
|  SUBSTR        |    주어진 값에 따라 자름   |
|   LEFT         |      왼쪽부터 N글자       |
|   LEFT         |     오른쪽부터 N글자       |
|   LENGTH       |     문자열 바이트 길이     |
| CHAR_LENGTH    |     문자열의 문자 길이     |
|   TRIM         |      양쪽 공백 제거        | 
|   LTRIM        |      왼쪽 공백 제거        | 
|   RTRIM        |      오른쪽 공백 제거      | 
|   LPAD(S,N,P)  |  S가 N글자 될때까지 P를 붙임|
|   RPAD(S,N,P)  |  S가 N글자 될때까지 P를 붙임|
|  REPLACE(S,A,B)|  S 중 A를 B로 변경         |
|  INSTR(S,s)    |S중 s의 첫위치반환, 없을 시 0|
|  CAST(A,T)     |  A를 T 자료형으로 변환     |
|  CURDATE       |     현재 날짜 반환         |
|  CURTIME       |     현재 시간 반환         |
|   NOW          |    현재 시간과 날짜 반환    |
|   DATE         |     문자열에 따라 날짜생성  |
|   TIME         |     문자열에 따라 시간생성  |
|   YEAR         |     주어진 DATETIME 연도   |
|   MONTHNAME    | 주어진 DATETIME 월(영문)   |
|   MONTH        |     주어진 DATETIME 월     |
|   WEEKDAY      |     주어진 DATETIME 요일값 |
|   DAYNAME      |   주어진 DATETIME 요일(영) |
|    DAY         |     주어진 DATETIME 날짜   |
|    HOUR        |     주어진 DATETIME 시     |
|    MINUTE      |     주어진 DATETIME 분     |
|    SECOND      |     주어진 DATETIME 초     |
|    ADDDATE     |    시간/ 날짜 더하기       |
|    SUBDATE     |    시간/ 날짜 뺴기         |
|    DAY_DIFF    |    두 시간/날짜 일수차      |
|    TIME_DIFF   |    두 시간/날짜 시간차      |
|    LAST_DAY    |    해당 달의 마지막날짜     |
|   DATE_FORMAT  |    시간/날짜 지정형식변환   |
|STR_TO_DATE(S,F)|    S를 F형식으로 해석 변경  |
|  IF(조건,T,F)  |  조건이 참이면 T, 거짓이면 F |
|  IFNULL(A,B)   |    A가 NULL일 시 B출력      |
|     ALL        |   서브쿼리의 모든 결과에 대해|
|     ANY        |   서브쿼리의 하나 이상의 결과|




 
- https://dev.mysql.com/doc/refman/8.0/en/numeric-functions.html
- https://dev.mysql.com/doc/refman/8.0/en/string-functions.html
- https://dev.mysql.com/doc/refman/8.0/en/string-functions.html
- %Y: 연도 4자리 / %y: 연도 2자리 / %M: 월 영문 / %m: 월 숫자
- %D: 일 영문 / %d: 일 숫자 / %T: hh:mm:ss  / %t: hh:mm:ss AM/PM


- EX) SELECT 'HELLO' LIKE 'HEL%';
- EX) SELECT 'HELLO' LIKE 'HEL__'; 


## MYSQL 설치
- utf8mb4 : 한글 포함 전세계 문자 + 이모티콘 가능
- utf8mb4_general_ci : 정렬속도 빠름

## MYSQL TABLE

|  CREATE TABLE     |      테이블 만들기             |
|  ALTER TABLE      |      테이블 변경               |
|  DELETE TABLE     |      테이블 제거               |
|  INSERT INTO      |      데이터 삽입               |
|  AUTO_INCREMENT   | 새 행 생성마다 1증가           |
|  PRIMARY KEY      |    중복입력 불가               |
|     UNIQUE        |    중복입력 불가               |
|    NOT NULL       |    NULL 입력 불가             |
|    UNSIGNED       |     양수(숫자)만 가능          |
|    DEFAULT        |   값 없을 시 기본값            |
|  DECIMAL(s,d)     | 실수 부분 총 자릿수, 소숫자리수 |
|      CHAR         |        고정사이즈              |
|    VARCHAR        |        가변사이즈              |
|    DELETE         |       주어진 조건 행 삭제      |
|    TRUNCATE       |      테이블 초기화             |
|    UPDATE         |     주어진 조건의 행 수정하기   |
