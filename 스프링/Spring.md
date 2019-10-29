# Spring

- 자바 애플리케이션 개발을 위한 오픈소스 프레임워크
- 프레임워크 vs library
  - 라이브러리: 애플리케이션 개발에 필요한 기능 제공, 우리의 코드가 라이브러리 사용
  - 프레임워크: 비지니스 로직이 빠진 뼈대만 갖춰진 애플리케이션(반제품)
    - ppt: framework + idea(business logic)
    - framework 접할 때 중요한것은? 사용법, 물론 원리를 알면 더 좋다!!
    - 개발자는 기술이 아닌 비지니스 로직에 집중해라!!!

- 프레임워크를 사용하면> 귀찮은 일들을 대신 해준다~
- JDBC를 한다면: DB 관리, TX, 쿼리 작성, JDBC 코드 작성, 예외 처리, 리소스 관리 --> 쿼리 작성

- light weight framework - 스프링 이전에는 EJB --> POJO(plane old java object)

  bean(스프링이 관리하는 자바 객체 - stateless 한 특성)의 container로써 동작

  DI & AOP

- 스프링 history(설정)

  - 1.0 --> xml 기반의 설정
  - 2.5 --> annotation 설정 추가(xml + annotation) - 유지보수 용이, 개발 속도는 조금 느림
  - 3.0 --> java config 기반 설정(java + annotation) - 유지보수 상대적으로 불편, 개발 속도는 빠름
  - boot --> 설정의 자동화
  - STS 4.0, eclipse plugin --> legacy를 지원하지 않는다.

- 스프링 DI(dependency injection)

  - 의존성?
    - 사용되는 멤버변수(객체)가 변경될 때 사용하는 클래스가 변경되어야하는 것 --> 유지보수성 안좋음, 그래서 의존성을 주입 받아서 쓰면 편이

- 스프링 애플리케이션 구성: POJO - 부품, Spring Framework(Container) - 자동 조립 로봇, 설정 메타 정보(xml, annotation, java bean) - 조립 메뉴얼

  - xml 기반의 빈 생성
  - xml + annotation 활용
    - component-scan : 소스 코드상에서 component를 찾는다 --> component = bean
    - 내가 소스를 가지고 있는 녀석들 --> scan이 빠르지만 3rd parth lib를 빈으로 사용할 때는?
    - 빈 대상 클래스에 @Component선언
    - @Autowired: 대상 빈을 타입 기반으로 연결
    - @Qualifier: 대상 빈을 이름 기반으로 연결
    - @Value: scalar(기본형, String) 값을 연결
    - @Component: 빈을 선언할 때 사용 --> 빈의 Object 레벨...
    - 스테레오타입 어노테이션:  세부적으로 용도에 맞춰서 빈 관리
      - @Service			: 서비스 클래스
      - @Repository   	:DAO 클래스
      - @Controller 	:웹에서 요청 처리하는 컨트롤러 타입 클래스
      - @Configuration	:Java config 기반의 환경 설정 파일
      - @Component	:잘 모를때
  - 빈 생성 기준
    1. @Autowired 선언된 생성자
    2. 기본생성자 호출로 빈 생성
    3. 모든 파라미터가 빈으로 선언된 생성자
    4. 위 3개에 부합한 생성자가 없으면 오류
  - 특정한 빈들로만 연결되는 프로젝트 구성
    - service - repository - TestImpl -- test환경에서만
    									- OperImpl -- 서비스환경에서
  - @Profile  -  사용할 빈들의 조합을 결정
  - runtime에 사용할 profile 지정
    - profile이 없는 빈들은 언제나 동작
    - profile이 지정된 녀석들은 profile이 선언될때만 동작