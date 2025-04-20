# Java Annotation

---

## 면접 질문 예시

> "Java의 Annotation(Component, Service, Repository, Controller)의 역할 및 차이를 설명해주세요.”

---

<details>
  <summary><h2> 평가 요소 및 모범 답안</h2></summary>

  ### 1. `@Component`
  - 포함내용
      - 역할 : 스프링이 관리하는 일반적인 빈(Bean)으로 등록할 때 사용하는 기본 어노테이션
      - 특징
        - 특정 계층에 속하지 않는 클래스(예: 유틸 클래스, 설정 클래스 등)에 사용합니다.
        - 컴포넌트 스캔 대상이 되어 Spring IoC 컨테이너에 자동 등록됩니다..


  </br>
  </br>


  ### 2. `@Service`
  - 포함내용
      - 역할 : 비즈니스 로직을 담당하는 서비스 계층(Service Layer) 클래스에 사용
      - 특징
        - 내부적으로는 @Component와 같지만, 의도를 명확히 나타내기 위한 의미적 구분입니다.
        - 가독성 향상과 유지보수에 도움이 됩니다.
        

  </br>
  </br>
  

  ### 3. `@Repository`
  - 포함내용
      - 역할 : 데이터베이스 연동을 담당하는 DAO 클래스(Persistence Layer)에 사용
      - 특징
        - @Component의 기능을 포함하면서, 추가로 스프링이 데이터 접근 예외를 DataAccessException으로 자동 변환해주는 기능이 내장되어 있습니다.
        - JPA, MyBatis 등 ORM 프레임워크와 함께 자주 사용됩니다.
        

  </br>
  </br>
    

  ### 4. `@Controller`
  - 포함내용
      - 역할 : 클라이언트의 요청을 받고 응답을 처리하는 웹 컨트롤러 클래스에 사용
      - 특징
        - Spring MVC 패턴의 컨트롤러로서 View를 반환하거나 Model을 처리합니다.
        - JSON 등 데이터 자체를 반환할 때는 @ResponseBody와 함께 사용하거나, @RestController를 사용합니다.
        

  </br>
  </br>

  
  ### 5. 모범 답안 예시

  > @Component는 스프링이 관리하는 일반적인 빈을 등록할 때 사용하는 어노테이션으로, 특정 계층에 속하지 않는 클래스에 주로 사용됩니다. </br>
  > 이는 컴포넌트 스캔을 통해 자동으로 스프링 컨테이너에 등록되며, 기본적인 빈 등록 어노테이션이라는 특징이 있습니다. </br>

  > @Service는 비즈니스 로직을 처리하는 서비스 계층 클래스에 사용되며, 내부적으로는 @Component와 동일하지만, 계층의 의미를 명확히 하기 위해 사용됩니다. </br>
  > 의미 기반의 구분을 통해 가독성과 유지보수성을 높이고, AOP 적용 시 의도를 명확히 할 수 있는 장점이 있습니다. </br>

  > @Repository는 데이터베이스와의 연동을 처리하는 DAO 클래스에 사용되며, @Component의 기능을 포함하면서도 데이터 접근 예외를 DataAccessException으로 변환하는 기능이 추가로 제공됩니다. </br>
  > 주로 JPA나 MyBatis 같은 ORM 기술과 함께 사용되며, Persistence 계층의 역할을 수행합니다. </br>

  > @Controller는 클라이언트의 HTTP 요청을 받아 처리하고, 뷰를 반환하거나 응답을 구성하는 웹 컨트롤러 클래스에 사용됩니다. </br>
  > Spring MVC 패턴에서 프레젠테이션 계층을 담당하며, 요청 매핑 어노테이션과 함께 사용되어 웹 서비스의 진입점 역할을 합니다. </br>


</details>
