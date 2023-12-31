# QnA

## Java

### 0. 객체?

- 객체는 객체 지향 프로그래밍의 가장 기본적인 단위이자 시작점이다.
- 우리 주변에서 흔히 볼 수 있는 모든 실재하는 대상을 객체라고 한다.
- 눈에 보이는 유형의 대상뿐 아니라 보이지 않는 논리, 사상, 철학, 개념, 공식 등 무형의 대상들도 포함될 수 있다

### 1. 객체지향 프로그래밍의 특징

- Object-Oriented Programming(OOP) 란, 여러 독립적인 부품들의 조합, 즉 객체들의 유기적인 협력과 결합으로 파악하고자 하는 컴퓨터 프로그래밍의 패러다임을 의미한다.

- 4가지 특징이 있다
    - 추상화 : 중복되는 코드를 제외하고 단일 객체에 정의함으로써 코드를 고도화하는것, 객체의 속성중 중요한 부분에 중점을 두어 개략화 하는것
    - 상속 : 기존의 클래스를 재활용하여 새로운 클래스를 작성하는 자바의 문법요소
    - 캡슐화 : 서로 연관있는 속성과 기능들을 하나의 캡슐로 만들어 데이터를 외부로부터 보호하는것 (접근제어자, getter/setter)
    - 다형성 : 어떤 객체의 속성이나 기능이 그 맥락에 따라 다른 역할을 수행할 수 있는 객체 지향의 특성(오버라이딩, 오버로딩)


### 2. JVM의 구조와 Java의 실행방식

- 구조
    - 클래스로더
    - 실행 엔진
    - 런타임 데이터 에어리어
    - JNI + Native Method Library

- 실행 방식
    - 자바 컴파일러가 .java 코드를 읽어 .class로 변환
    - 클래스 로더를 통해 JVM으로 로딩
    - 실행 엔진을 통해 해석
    - Runtime data area에 배치되어 실질적 수행

### 3. GC

- 메모리영역에서 사용하지 않는 객체들을 제거하는 작업을 총칭

### 4. 컬렉션 프레임워크

- Java Collection은 객체, 데이터들을 효율적으로 관리 할 수 있는 자료구조들이 있는 라이브러리

- Collection 인터페이스 
    - List 인터페이스 : 순서가 있는 집합 자료구조로 데이터의 중복을 허용합니다.
    - Set 인터페이스 : 순서가 없는 집합 자료구조로 데이터의 중복을 허용하지 않습니다.

- Map 인터페이스 : 키와 값의 한쌍으로 이루어지는 데이터의 집합으로, 순서가 없으며 키는 중복을 허용하지 않지만, 값은 중복을 허용합니다.

### 5. 어노테이션

- 인터페이스를 기반으로 한 문법, 주석처럼 코드에 달아 클래스에 특별한 의미를 부여하거나 기능을 주입

### 6. 오버라이딩, 오버로딩의 차이

- 오버라이딩은 상위 클래스의 메서드를 재정의하는것
- 오버로딩은 같은 클래스 내의 동일한 이름을 가진 메서드가 매개변수의 타입, 개수가 다르게 구현할 수 있는것

### 7. 인터페이스, 추상클래스

- 추상클래스는 객체의 추상적인 상위 개념으로 공통된 개념을 표현할 때 사용, 단일 상속만 가능
- 인터페이스는 구현 객체가 같은 동작을 한다는 것을 보장하기 위해 사용, 다중 상속 가능

### 8. 동일성, 동등성

- 동일성은 객체의 주소를 비교하는것
- 동등성은 객체의 같음을 비교하는것

### 9. 원시타입, 참조타입

- 원시타입은 Java에서 단 8개밖에 존재하지 않는 타입.
    - boolean(1byte), byte(1byte), char(2byte), short(2byte), int(4byte), float(4byte), long(8byte), double(8byte)
- 원시타입 외 모든 타입, Object 클래스 이거나 이를 상속하는 클래스

### 10. Java8에서 추가된 기능

- Lambda(함수형 프로그래밍 지원), Stream(고차함수 지원), Optional(null-safety제공, stream과 유사) 등이 추가


### 11. 지네릭

- 클래스나 메서드에서 사용할 내부 데이터 타입을 컴파일 시에 미리 지정하는 방법입니다.
- 클래스나 메서드에서 사용되는 객체의 타입 안정성을 높일 수 있습니다.
- 반환값에 대한 타입 변환 및 타입검사에 들어가는 노력을 줄일 수 있습니다.

### 12. Static(정적)

- 정적(static)은 고정된이란 의미를 가지고 있습니다. Static이라는 키워드를 사용하여 Static변수와 Static메소드를 만들 수 있는데 다른말로 정적필드와 정적 메소드라고도 하며 이 둘을 합쳐 정적 멤버라고 합니다. (클래스 멤버라고도 합니다.)
- Java에서 Static 키워드를 사용한다는 것은 메모리에 한번 할당되어 프로그램이 종료될 때 해제되는 것을 의미합니다.

----------------------------------------------------------------------------

## Spring

### 1. IOC

- 제어의 역전, 프로그램의 제어 흐름을 개발자가 제어하는것이 아닌 스프링에게 위임하는것

### 2. DI

- 의존관계 주입, IOC의 형태로 클래스 사이의 의존관계를 빈 설정 정보를 바탕으로 컨테이너가 자동 연결하는것

### 3. Bean

- IOC 컨테이너안에 들어있는 객체, 필요할 때 IOC 컨테이너에서 가져와 사용 @Bean으로 설정가능

### 4. IOC 컨테이너의 역할

- 어플리케이션 실행 시점에 빈 오브젝트를 인스턴스화 하고 DI 한 후에 최초로 어플리케이션을 기동할 빈 하나를 제공

### 5. DI의 종류

- 생성자 : 생성자 호출 시점에 딱 한번만 호출, 불변, 필수 의존관계에 사용
- Setter : 선택, 변경 가능성이 있는 의존관계에 사용, 스프링 빈을 선택적으로 등록 가능
- 필드 주입 : @Autowired 를 사용, 외부에서 변경이 불가하여 테스트 하기 힘들며, DI프레임워크 없이는 작동하기 힘들다

### 6. MVC

- 디자인패턴, Model, View, Controller 3가지로 나누어 역할을 분리후 처리하는 패턴
    - Model : 어플리케이션의 데이터, 모든 데이터 정보를 가공하여 가지고 있는 컴포넌트
    - Veiw : 시각적인 UI 요소를 지칭, Model, Controller에 대한 정보를 알면 안되며 단순히 표시하는 역할
    - Controller : Model, View를 연결해주는 역할을 한다

### 7. VO

- Value Object의 줄임말로, 값을 가지고 있는 객체입니다.
- 비즈니스 값을 가져올때 사용하며, 보통 값을 수정할 수 없는것으로 합니다. DTO와 혼용해서 사용하기도 합니다.

### 8. DTO

- Data Transfer Object의 줄임말로, VO와같이 값을 가지고 있는 객체입니다.
- VO와 차이점은 DB로 치자면 하나의 인스턴스로, 데이터 핸들링에 사용되는 객체입니다. DTO를 통해 데이터를 전달할 수 있습니다.


### 9. DAO

- Data Access Object의 줄임말로, 실제 데이터베이스에 접속하는 객체입니다.


### 10. AOP

- Aspect Oriented Programming, 관점 지향 프로그래밍이라 합니다. 어떤 로직을 기준으로 핵심적인 관점, 부가적인 관점으로 나누어서 보고 그 관점을 기준으로 모듈화 하겠다는 것입니다.
- 스프링 프레임워크의 핵심요소중 하나로, 비즈니스 로직과 공동 모듈을 분리하고, 핵심로직 사이사이에 공동모듈을 잘 끼워넣는것을 말합니다.
- 이때 공동모듈을 코드 밖에서 설정된다는것이 핵심입니다. 인증, 로깅, 트랜잭션 처리에 용의합니다.

### 11. Intercepter, Filter

- 공통점은 Controller가 호출되기 전에 실행됩니다.
- 차이점은 Filter는 dispatcher가 호출되기 전에, Intercepter는 dispatcher가 호출되고 난 이후에 호출됩니다.
- 인코딩이나 보안같은 WebApp에 전역적으로 처리해야 할 경우 Filter를 사용합니다.
- 클리이언트의 요청에 따른 인증, 권한등의 디테일한 처리는 Intercepter에서 처리 합니다.

-----------------------------------------------------------------------------------------------------
## JPA

### 1. Entity

- 실제 데이터베이스의 테이블과 1대1로 맵핑되는 클래스

### 2. N+1 문제

- 1번의 쿼리를 날렸을 때 의도하지 않은 N번의 쿼리가 추가적으로 실행되는 것을 의미한다.
- Lazy로딩에 의해 한번에 모든 정보를 가져오지 않아서 발생하는 문제, 패치 조인을 사용해서 해결할 수 있다

### 3. JPA 영속성 컨텍스트의 이점

- 영속성 컨텍스트는 엔티티를 영구 저장하는 환경을 의미합니다
- 1차캐시 : 조회가 가능하며, 1차캐시에 없으면 DB에서 조회하여 1차캐시에 올려놓습니다.
- 동일성 보장 : 동일성 비교가 가능합니다.(==)
- 쓰기 지연 : 트랜잭션을 지원하는 쓰기지연이 가능하며, 트랜잭션을 커밋하기 전까지 SQL을 바로 보내지 않고 모아서 보낼수 있습니다.
- 변경감지 : 스냅샷을 1차캐시에 들어온 데이터를 찍습니다. 커밋되는 시점에 Entity와 스냅샷을 비교하여 update SQL을 생성합니다.
- 지연로딩 : Entity에서 해당 Entity를 불러올때 SQL을 날려 해당 데이터를 가져옵니다.

-----------------------------------------------------------------------------------------------------------------

## DB

### 1. 트랜잭션

- 데이터베이스의 상태를 변화시키는 작은 단위
- 트랜잭션 하나가 전부 반영되던지 아예 반영이 안되던지 둘중 하나

### 2. index의 특징

- 데이터베이스 검색 속도 향샹을 위한 자료구조


-------------------------------------------------------------------------------------------------------

# 면접 기술 테스트

## QNA

### Q. MVC 패턴에 대해 아는것을 서술하세요

### A. MVC는 Model, View, Controller 의 약자입니다.

- 하나의 어플리케이션, 프로젝트를 구성할 때 그 구성요소를 세가지 역할로 구분한 디자인 패턴입니다.
- 사용자가 보는 페이지, 데이터처리, 그리고 이 2가지를 중간에서 제어하는 컨트롤, 이 3가지로 구성되는 하나의 애플리케이션을 만들면 각각 맡은바에만 집중을 할 수 있게 됩니다.
- 유지보수에 유리하고, 애플리케이션의 확장성, 그리고 유연성이 증가하며, 중복코딩이라는 문제점 또한 사라지게 됨에 이점이 있습니다.

### Model

- 어플리케이션의 정보, 데이터를 나타냅니다. 
- 데이터 베이스, 처음에 정의하는 상수, 초기화 값, 변수 등을 뜻합니다.

### View

- input 텍스트, 체크박스 항목 등과 같은 사용자 인터페이스 요소를 나타냅니다.
- 데이터 및 객체의 입력, 보여주는 출력을 담당, 데이터 기반으로 사용자들이 볼 수 있는 화면입니다.

  ### Controller

  - 데이터(Model)와 사용자 인터페이스 요소(View)들을 잇는 다리역할을 합니다.
  - 사용자가 데이터를 클릭하고, 수정하는 것에 대한 이벤트들을 처리하는 부분을 뜻한다.

------------------------------------------------------------------------------------------------------------------

### Q. JOIN 에대해 아는것을 서술하세요

### A. 관계형 데이터베이스의 테이블 안에 있는 행들을 논리에 따라 연결할 수 있도록 하는 기법입니다.

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
 

### Q. TO_CHAR

### A. 오라클에서 쿼리문을 작성할 때 날짜, 숫자등의 값을 문자열로 반환합니다.

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

### Q. DECODE

### A. 프로그래밍의 IF-ELSE 논리를 제한적으로 구현한 DBMS 메서드 입니다.

- DECODE(컬럼, 조건1, 결과1, 조건2, 결과2... ,'DEFAULT_RESULT');



  
