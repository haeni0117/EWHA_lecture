# 멀티플렉서(multiplexer)
여러개의 데이터 입력 -> 한 개 이상의 선택입력 -> 한 개의 출력 : 여러 개의 데이터에서 하나의 출력 by 선택입력
## 선택입력 : 여러 개의 데이터 중 하나를 출력으로 선택한다
SOP(sum of products)로 나타낼 수도 있고, transmission gate회로로 나타낼 수도 있다.
### 2-to-1 multiplexer
2개의 데이터(w0,w1), 1개의 선택입력(s)
작은 멀티플렉서를 여러 개 이용하여 큰 멀티플렉서를 구현할 수 있다 ex) [2-to-1]*3=> 4-to-1 multiplexer
### 4-to-1 multiplexer
4개의 데이터(w0,w1,w2,w3), 2개의 선택입력(s0,s1)
### nxk 크로스바스위치(crossbar switch) : n개의 입력 중 임의의 하나를 k개의 출력 주 임의의 하나로 연결하는 회로
입력과 출력의 수가 서로 다른 다양한 크기의 크로스바 스위치를 만들 수 있음 ex)2x2크로스바 스위치 : 입력 2개, 출력 2개
#### ex) 그림 4.5b : 2-to-1 multiplexer를 사용하여 2x2 크로스바 스위치를 구현한다
- 선택 입력 s에 의해 멀티플렉서의 입력이 선택된다.
- if s=0 ) x1 -> y1 & x2 -> y2
- if s=1 ) x1 -> y2 & x2 -> y1
- 크로스바 스위치 : 한쪽의 선들 중에 하나를 선택하여 다른 쪽의 선 중에 하나로 연결함
- 그 연결형태가 변하는 응용분야에 유용하게 사용된다
# 멀티플렉서를 사용한 논리함수 구현
### 멀티플렉서(multiplexer)
- 실질적인 응용분야에서 유용하다
- 논리함수를 직접 구현하는 데 사용될 수 있음
- ex) f = w1 XOR w2
  - 4-to-1 멀티플렉서의 입력에 진리표의 출력을 상수(constant)로 연결하여 함수 구현 가능하다
  - 출력 f : 진리표에 대응하는 함수값
  - 직관적이지만 비효율적임(-)
- cf) 한 개의 2-to-1 멀티플렉서를 사용하여 f를 구현한다
  - how? 입력신호 중 하나인 w1을 2-to-1 멀티플렉서의 선택입력(s)으로 정한다.
  - ex) 입력이 3개인 다수결 함수(majority function)에 대해 진리표수정
    - 수정전 : 입력 3개(w1,w2,w3)
    - 수정후 : 세 개의 입력 중 임의의 두 개 입력을 멀티플렉서의 선택입력으로 선택한다.
    - 

