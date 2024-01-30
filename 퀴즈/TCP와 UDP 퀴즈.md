<b>※ INDEX</b> <br>
<code>  </code> : 핵심 키워드

### 1. TCP의 장단점에 대해 설명해주세요.
<details>
  <summary>답</summary>
  <br>
  <b>장점</b>
  <li>데이터의 순서를 보장하므로, <code>신뢰성 있는 데이터 전송</code>이 가능하다</li>
  <li>연결 지향 방식과 재전송 매커니즘을 통한 <code>패킷 손실을 방지</code>한다</li>
  <br>
  <b>단점</b>
  <li><code>연결 설정 및 종료 과정</code>으로 인해 <code>느린 속도</code></li>
  <li>패킷 손실 발생 시 <code>재전송</code>을 통해 속도가 더욱 느려질 수 있다</li>
  <br>
</details>

### 2. 3-way Handshake 과정을 설명해주세요.
<details>
  <summary>답</summary>
  <br>
  <i><code>TCP</code>에서 데이터를 전송하기 전 <code>수신자와 송신자 간 연결을 설정하는 과정</code></i>
  <br><br>
  <b>1. Client → Server <code>[SYN]</code></b>
  <p>클라이언트가 서버에게 <code>통신을 시작하기 위한 요청</code>을 보내며 SYN flag 가 설정된 패킷을 보낸다.<br>
    이 때 클라이언트는 초기 sequence number 를 랜덤하게 선택하여 전송한다</p>
  <b>2. Server → Client <code>[SYN/ACK]</code></b>
  <p>서버는 SYN 요청을 받고 클라이언트의 <code>연결 요청을 수락</code>한다는 ACK와 SYN flag 가 설정된 패킷을 보낸다. <br>
    이 때 ACK는 클라이언트의 sequence number +1, SYN 은 서버의 임의의 sequence number로 설정한다 </p>
  <b>3. Client → Server <code>[ACK]</code></b>
  <p>클라이언트가 서버에게 ACK를 보내면서 <code>연결을 설정</code>한다. <br>
    이 때 ACK는 서버의 sequence number +1</p>
  <br>
</details>

### 3. UDP의 특징을 설명해주세요.
<details>
  <summary>답</summary>
  <br>
  <li><code>비연결성</code> : 연결을 설정하지 않고 데이터를 전송한다</li>
  <li><code>낮은 신뢰성</code> : 데이터 전송의 정확성을 보장하지 않는다</li>
  <li><code>고속 전송</code> : 연결 설정 및 제어 매커니즘이 없어서 더 빠른 속도로 데이터 전송이 가능하다</li>
  <li><code>동시 전송</code> : 멀티캐스트, 브로드캐스트를 지원하여 여러 수신자에게 동시에 전송이 가능하다</li>
  <br>
</details>

### 4. UDP의 Checksum 검사 방식에 대해서 설명해주세요.
<details>
  <summary>답</summary>
  <br>
  <b>1. 송신자</b><br>
  <p><code>보낼 UDP 패킷의</code> 헤더와 데이터를 합쳐서 <code>Checksum을 계산</code>하고, 이 값을 UDP <code>헤더에 추가</code>한다</p></p>
  <b>2. 수신자</b><br>
  <p><code>받은 UDP 패킷의</code> 헤더와 데이터를 합쳐서 <code>Checksum 값을 계산</code>하고, <code>계산된 Checksum 값과 패킷 헤더의 Checksum 값을 비교</code>한다</p>
  <b>3. 오류 검출</b><br>
  <p><code>Checksum 값이 일치하면 데이터에 오류가 없다고 가정</code>하고 처리한다.<br> 
    그렇지 않을 경우 데이터에 오류가 있을 가능성이 높으며, <code>오류는 애플리케이션 단에서 처리</code>하므로 애플리케이션에 따라 처리 방법이 상이하다</p>
</details>
