<details>
  <summary><strong>현대 컴퓨터 시스템에서 I/O 장치를 다양한 버스 계층으로 나누어 연결하는 이유는 무엇인가요?</strong></summary>

  I/O 장치를 다양한 버스 계층으로 나누는 이유는 성능과 비용의 균형을 맞추기 위해서입니다.  
  고속의 메모리 버스는 장치와 CPU 사이에서 높은 데이터 전송 속도를 제공하지만, 비용이 비싸고 길이가 제한적입니다.  
  따라서, 고성능 장치(예: 그래픽 카드)는 CPU와 가까운 고속 버스(PCI 또는 PCIe)에 연결하고, 저속 장치(예: 마우스, 디스크)는 저속 주변장치 버스(SATA, USB)에 연결합니다.
  이렇게 함으로써 고속 장치의 성능을 최대화하면서 비용을 절감할 수 있습니다.
</details>

<details>
  <summary><strong>표준 장치(Canonical Device)의 주요 구성 요소는 무엇이며, 각각의 역할은 무엇인가요?</strong></summary>

   표준 장치는 인터페이스와 내부 구조라는 두 가지 주요 구성 요소로 이루어져 있습니다.  
   인터페이스는 장치가 시스템 소프트웨어와 상호작용하는 수단을 제공하며, 상태(Status), 명령(Command), 데이터(Data) 레지스터로 구성됩니다.  
   내부 구조는 장치의 실제 동작과 관련된 하드웨어를 포함하며, 장치 고유의 동작을 처리하는 펌웨어나 특수화된 하드웨어가 있을 수 있습니다.  
   이러한 구조는 운영체제가 장치를 추상화하여 제어할 수 있도록 돕습니다.
</details>

<details>
  <summary><strong>폴링(Polling)과 인터럽트(Interrupt)의 차이점과 각각의 장단점에 대해 설명해보세요.</strong></summary>

  폴링은 CPU가 장치의 상태를 지속적으로 확인하여 작업 완료 여부를 확인하는 방식입니다.  
  반면, 인터럽트는 장치가 작업 완료 시 CPU에 신호를 보내 작업 완료를 알립니다.  
  폴링은 구현이 단순하고 빠른 작업에서 효율적이지만, CPU 자원을 낭비하기 쉽습니다.  
  반대로, 인터럽트는 CPU가 다른 작업을 수행할 수 있도록 해 효율적이지만, 처리 오버헤드와 컨텍스트 스위칭 비용이 발생합니다.  
  빠른 장치에서는 폴링이, 느린 장치에서는 인터럽트가 더 적합합니다.
</details>

<details>
  <summary><strong>Direct Memory Access(DMA)가 CPU 중심의 데이터 전송 방식에 비해 가지는 장점은 무엇인가요?</strong></summary>

  DMA는 CPU의 개입 없이 메모리와 장치 간 데이터를 직접 전송할 수 있는 방식입니다.  
  이를 통해 CPU는 데이터 전송과 같은 단순 작업에서 벗어나 다른 중요한 작업을 수행할 수 있습니다.  
  또한, 대량의 데이터를 전송할 때 효율적이며, CPU가 병목현상이 되는 것을 방지하여 시스템 전체 성능을 향상시킬 수 있습니다.
  </details>

<details>
  <summary><strong>디바이스 드라이버의 역할과 이를 통해 운영체제가 얻는 이점은 무엇인가요?</strong></summary>

  디바이스 드라이버는 운영체제와 하드웨어 장치 간의 중간 역할을 수행하는 소프트웨어입니다.  
  이를 통해 운영체제는 장치의 세부 구현을 알지 않고도 통일된 인터페이스로 다양한 장치를 제어할 수 있습니다.  
  이로 인해 운영체제는 장치 독립성을 확보할 수 있으며, 새로운 장치가 추가되더라도 해당 장치에 맞는 드라이버만 제공되면 기존 시스템과 쉽게 통합될 수 있습니다.
  </details>