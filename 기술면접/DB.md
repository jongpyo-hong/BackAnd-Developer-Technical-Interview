# QnA

## DB

### 1. 트랜잭션

- 데이터베이스의 상태를 변화시키는 작은 단위
- 트랜잭션 하나가 전부 반영되던지 아예 반영이 안되던지 둘중 하나

### 2. index의 특징

- 데이터베이스 검색 속도 향샹을 위한 자료구조


### 3. JOIN 에대해 아는것을 서술하세요

- 관계형 데이터베이스의 테이블 안에 있는 행들을 논리에 따라 연결할 수 있도록 하는 기법입니다.

- 데이터베이스에 저장 되어있는 데이터들은 각 테이블안에 흩어져 저장되어 있으므로, 사용자 원하는 형태로 데이터를 조작하려면 특별한 방법이 필요한데 그것이 조인 입니다.

    ### INNER JOIN(내부조인)

    - 여러 애플리케이션에서 사용되는 가장 흔한 결합 방식이며 기본 조인 형식으로 간주됩니다 (INNER는 생략가능).
    - 테이블 사이에 열거하는 모든 조건이 일치하는 결과 집합을 반환합니다.

    ### OUTER JOIN(외부조인)

    - INNER JOIN이 모든조건을 만족하는 조합만을 조회한다면, OUTER JOIN은 컬럼 값이 NULL등 알 수 없는 경우에도 결과 집합을 조회 합니다.
    - 조회 결과의 중심을 어디에 두느냐에 따라서 LEFT OUTER, RIGHT OUTER, FULL OUTER JOIN으로 나눌수 있습니다.

        #### LEFT OUTER JOIN

        - 조인문 왼쪽에 있는 테이블의 모든 결과를 가져온 후 오른쪽의 테이블 데이터를 매칭, 매칭되는 데이터가 없을 경우 NULL값으로 표시합니다.

        #### RIGHT OUTER JOIN

        - 조인문 오른쪽에 있는 테이블의 모든 결과를 가져온 후 왼쪽의 테이블 데이터를 매칭, 매칭되는 데이터가 없을 경우 NULL값으로 표시합니다.

        #### FULL OUTER JOIN

        - LEFT OUTER JOIN과 RIGHT OUTER JOIN을 합친것으로, 양쪽 모두 조건이 일치하지 않는 데이터까지 모두 출력합니다.
 

### 4. TO_CHAR

- 오라클에서 쿼리문을 작성할 때 날짜, 숫자등의 값을 문자열로 반환합니다.

    - 1. 날짜 포맷 변경 : SELECT TO_CHAR(SYSDATE, 'YYYY-MM-DD') - 2023-06-23
    
    - 2. 소수점 변경 : SELECT TO_CHAR(123.456, 'FM990.999') - 123.456
                    SELECT TO_CHAR(0.12345, 'FM9990.99') - 0.12
        *FM : 문자열의 공백제거 숫자의 최대 길이만큼 9999. 형식을 지정합니다 (9 : 값이 없으면 표시안함, 0: 값이 없으면 "0"으로 처리)
            정수은 지정한 형식보다 값의 길이가 길면 오류, 소수 지정한 길이보다 길면 반올림
    
    - 3. 숫자의 천단위 콤마 찍기 : SELECT TO_CHAR(12367, 'FM999,999') - 123,467
                                SELECT TO_CHAR(123467, 'FML999,999') - ￦123,467

    - 4. 지정한 길이만큼 0으로 채우기 : SELECT TO_CHAR(123) - 123
                                    SELECT TO_CHAR(123, 'FM00000') - 00123

    - 5. 날짜에 0 없애기 : SELECT TO_CHAR(SYSDATE, 'MM/DD') - 06/23 (날짜 포맷 변경)
                        SELECT TO_CHAR(SYSDATE, 'FMMM/DD') - 6/23

    - 6. 임의의 구분자로 날짜형식 만들기 : SELECT TO_CHAR('""YYYY"년 "MM"월 "DD"일"') - 2023년 06월 23일
                                        SELECT TO_CHAR('""HH24"시 "MI"분 "SS"초"') - 12시 27분 32초

    - 7. 시간의 오전, 오후값 반환 : SELECT TO_CHAR(SYSDATE, 'AM') - 오전
                                SELECT TO_CHAR(SYSDATE, 'AM HH:MI:SS') - 오전 12시 30분 20초

    - 8. 날짜의 요일 반환 : SELECT TO_CHAR(SYSDATE, 'D') - 6 (1(일)~7(토))
                        SELECT TO_CHAR(SYSDATE, 'DY') - 금
                        SELECT TO_CHAR(SYSDATE, 'DAY') - 금요일

    - 9. 1년기준 몇일, 몇주 분기 반환 : SELECT TO_CHAR(SYSDATE, 'DDD') - 174 (365일 기준 몇일)
                                    SELECT TO_CHAR(SYSDATE, 'WW') - 25 (1년(52주)기준 몇주)
                                    SELECT TO_CHAR(SYSDATE, 'Q') - 2 (몇분기)

    - 10. 간편한 날짜 변환 : SELECT TO_CHAR(SYSDATE, 'MON') - 6월
                            SELECT TO_CHAR(SYSDATE, 'DL') - 2023년 6월 23일 금요일

### 5. DECODE

- 프로그래밍의 IF-ELSE 논리를 제한적으로 구현한 DBMS 메서드 입니다.

- DECODE(컬럼, 조건1, 결과1, 조건2, 결과2... ,'DEFAULT_RESULT');



  
