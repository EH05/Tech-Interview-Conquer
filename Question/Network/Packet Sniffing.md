# Packet Sniffing

---

## 면접 질문 예시

> "패킷 스니핑(Packet Sniffing)이란 무엇이며, 네트워크 보안 측면에서 어떤 위협을 줄 수 있는지 설명해 주실 수 있나요?"

---

<details>
  <summary><h2>평가 요소 및 평가 요소 별 모범 답안</h2></summary>

  ### 1. 패킷 스니핑의 정의
  - 포함내용:
    - 네트워크 상을 오가는 패킷을 몰래 가로채어 분석하는 행위.
    - NIC를 프로미스큐어스(promiscuous) 모드로 설정하거나 허브/스위치 미러링 포트를 이용하여 수행.
  - <details>
    <summary>모범 답안 예시 :</summary>
    
      > "패킷 스니핑은 네트워크 인터페이스 카드를 프로미스큐어스 모드로 동작시켜, 내게 전달된 패킷뿐 아니라 네트워크 상에 흐르는 모든 패킷을 캡처하고 분석하는 기법입니다."
    </details>

  ### 2. 스니핑 동작 원리
  - 포함내용:
    - 이더넷 허브 환경 vs 스위치 환경에서의 차이점.
    - 포트 미러링, ARP 스푸핑 등을 통한 스니퍼 위치 확보 방법.
  - <details>
    <summary>모범 답안 예시 :</summary>
    
      > "허브에서는 모든 트래픽이 브로드캐스트되어 쉽게 캡처되지만, 스위치 환경에서는 스패닝 포트(포트 미러링)나 ARP 스푸핑을 활용해 특정 호스트의 트래픽을 가로채야 합니다."
    </details>

  ### 3. 보안 위협 및 영향
  - 포함내용:
    - 기밀 정보(비밀번호, 세션 토큰, 개인 데이터) 유출.
    - 세션 하이재킹, 인증 크리덴셜 탈취, 내부 네트워크 구조 파악.
    - 중간자 공격(MITM) 전단계로 활용 가능.
  - <details>
    <summary>모범 답안 예시 :</summary>
    
      > "스니핑을 통해 로그인 쿠키나 평문 비밀번호를 탈취할 수 있으며, 이를 바탕으로 세션 하이재킹이나 MITM 공격을 수행할 수 있어 사용자의 민감 정보가 심각하게 노출됩니다."
    </details>

  ### 4. 심화 지식 : 대응 및 방어 대책
  - 포함내용:
    - 전송 계층 암호화(TLS/SSL), VPN, SSH 터널링 등 암호화된 통신 사용.
    - 무선 환경에서 WPA2/WPA3 같은 강력한 암호화 프로토콜 적용.
    - 네트워크 분할(세그멘테이션), 포트 보안, ARP 스푸핑 방지(동적 ARP 검사).
    - IDS/IPS, 스니퍼 탐지 도구(예: arpwatch) 활용.
  - <details>
    <summary>모범 답안 예시 :</summary>
    
      > "민감 데이터를 전송할 때는 반드시 TLS나 VPN을 사용해 패킷 내용이 암호화되도록 해야 하며, 스위치에서는 동적 ARP 검사(DAI)와 포트 보안 설정을 통해 ARP 스푸핑을 차단하고, IDS/IPS 시스템으로 비정상적 패킷 캡처 시도를 탐지해야 합니다."
    </details>

</details>
