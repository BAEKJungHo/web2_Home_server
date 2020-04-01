# web2_home_server

> [생활코딩 인프런 강의 web2_Home_server](https://www.inflearn.com/course/web2-home-server)

- 목표
  - 공유기가 연결된 환경에서 웹 서버를 구동하는 방법을 알려주는 수업
  - 공유기가 연결된 웹 서버에 특정 다수가 접속하게 하는것은 쉬운일이 아님

## 공유기(Router)

스마트폰, 노트북, 컴퓨터 등 공유기와 연결되는 순간 IP 를 부여받는다. 공유기도 마찬가지로 아이피를 부여 받는다 (192.168.0.1) 같은 형식이다. 
공유기에 부여되는 IP 는 중요해서 이름이 있는데 `Gatewaye address, Routeraddress` 라고 한다.

스마트폰, 노트북, 컴퓨터 등에 부여된 IP 는 `private IP address` 내선번호라고 생각하면된다. 공유기 뒷편에 통신사 케이블과 연결된 구멍은 WAN
인데, 여기에 부여되는 아이피는 `public IP address`

## NAT(Network Address Translation)

만약 우리가 192.168.0.4 의 private ip address 를 가지고 있으며 위키피디아에 요청을 보낼 경우 먼저 공유기의 192.168.0.1 를 통해 WAN 을 통해 외부로 보내게 된다. 이때 두 가지 현상이 발생한다.

- 우리의 private ip address 를 공유기에 기록(192.168.0.4)
- NAT 기술을 이용해 기록된 IP 를 public ip address 로 바꿔서 WAN 을 통해 외부로 요청(192.168.0.4 > 59.6.66.238)
