# Java의 접근제어자

---

## 면접 질문 예시

> "Java에서 접근 제어자에 대해 설명해주세요.”

---

<details>
  <summary><h2> 평가 요소 및 모범 답안</h2></summary>

  ### 1. 접근 제어자 종류
  - 포함내용
      - public
        - 어디서든 접근 가능 (같은 클래스, 같은 패키지, 다른 패키지 모두 가능)
        - 어떤 클래스나 메서드를 외부에서도 자유롭게 사용하게 하고 싶을 때 사용
      - protected
        - 같은 패키지 + 상속받은 클래스에서만 접근 가능
        - 외부 패키지여도 상속 관계라면 접근 가능
        - 주로 상속 구조에서 자식 클래스가 부모 클래스의 기능을 사용할 수 있게 할 때 사용
      - (default)
        - 같은 패키지 내에서만 접근 가능
        - 패키지 외부에서는 접근 불가
        - 패키지 단위로 기능을 묶을 때 사용
      - private
        - 해당 클래스 내부에서만 접근 가능
        - 외부 클래스, 자식 클래스 모두 접근 불가
           
  
  </br>
  </br>
  
</details>
