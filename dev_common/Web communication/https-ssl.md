## HTTPS / SSL 암호화
1. 대칭키

2. 공개키
- 공개키는 누구나 다운로드 받을 수 있다. / 복호화는 비공개키로만 가능하다.
- 장점 : 키를 전달할 때 중간에 가로채도 문제가 없다.
- 인증서에 사용됨. ( 공개키를 이용한 인증 )
- 비공개키를 사용해 정보를 암호화 한 후 공개키를 가진 사람에게 전달

### SSL 인증서
1. 클라이언트가 접속한 서버가 신뢰할 수 있는 서버임을 보장한다.
2. SSL 통신에 사용할 공개키를 클라이언트에게 제공한다.