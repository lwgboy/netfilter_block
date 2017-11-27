# netfilter_block
netfilter_block to filter a URL

# Usage
argv[1]에 막을 url 입력 <br />
./netfilter_block [막을 url]

# Code 분석
106~121 라인이 제일 중요 <br />
Host:에서 제공된 url 이 일치하면 전역변수 1을 0으로 변환 <br />

또한 cb 함수 내부의 132 라인의 <br />

`    
return nfq_set_verdict(qh, id, flag, 0, NULL); // flag: 1 ACCEPT, 0 DROP
`    
<br />
가 verdict의 두 번째 인자인 전역 변수 flag를 통해 Accept과 Drop 판단 <br />
나머지는 기본 코드와 동일함.
