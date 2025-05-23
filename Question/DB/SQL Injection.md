# SQL Injection

---

## 면접 질문 예시

> "SQL Injection 공격이 무엇이며, 이를 방지하기 위한 보안 방법에는 어떤 것들이 있는지 설명해 주세요”

---

<details>
  <summary><h2> 평가 요소 및 모범 답안</h2></summary>

  ### 1. SQL Injection의 개념 및 특징
  - 포함내용
    * SQL Injection의 개념 및 특징
      - 공격자가 웹 애플리케이션의 입력 필드에 악의적인 SQL 구문을 삽입하여, 원래 의도하지 않은 방식으로 데이터베이스를 조작하거나 조회하는 공격 방식입니다.
      - 데이터 탈취, 데이터 변조 및 삭제, 서버 내부 정보 노출 등의 문제가 발생할 수 있습니다.

  ### 2. SQL Injection을 방지하기 위한 보안 방법
  - 포함내용
    * Prepared Statements (Parameterized Query) → 가장 효과적인 방법
      - SQL 쿼리를 문자열로 직접 조작하지 않고, 매개변수로 분리해서 쿼리를 실행합니다.
      - 입력값은 쿼리 구조와 분리되므로, SQL 코드로 해석되지 않고 단순 데이터로 처리됩니다.
    * ORM 사용
      - ORM을 사용하면 SQL 구문을 직접 작성하지 않아도 되므로, 내부적으로 파라미터 바인딩을 사용하여 SQL Injection 위험을 줄여줍니다.
    * 입력값 검증 및 필터링
      - 예상하지 않은 형식의 데이터는 거부하거나, 화이트리스트 기반으로 검증합니다.
      - 예: 이메일, 숫자, 아이디 등 정규식 검증
    * 최소 권한 원칙
      - DB 계정에 불필요한 권한을 부여하지 않습니다.
      - 예: SELECT만 필요한 API는 INSERT, DELETE 권한 없이 구성
    * 에러 메시지 감추기
      - SQL 에러 메시지를 그대로 클라이언트에게 반환하지 않도록 처리합니다.
      - 이유: 공격자가 DB 구조 및 필드명을 추측할 수 있음
  
  ### 3.모범 답안 예시

  > SQL Injection은 공격자가 웹 애플리케이션의 입력 필드에 악의적인 SQL 구문을 삽입하여, 원래 의도하지 않은 방식으로 데이터베이스를 조작하거나 조회하는 공격 방식입니다.<br />
  > 이를 방지하기 위해 다양한 방식들이 존재합니다.<br />
  > 가장 대표적인 방식은 Prepared Statesments로, SQL 쿼리를 문자열로 직접 조작하지 않고 매개별수로 문리해서 실행하는 것입니다.<br />
  > 입력값은 쿼리 구조와 분리되기 때문에 SQL 코드로 해석되지 않고 단순 데이터로 처리됩니다.<br />
  > 이외에도 ORM 사용, 정규식을 활용한 입력값 검증 및 필터링, 불필요한 권한 부여 방지, 에러 메시지 반환 금지 등 다양한 방법이 있습니다.<br />
  
</details>
