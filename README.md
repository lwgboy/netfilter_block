# netfilter_block
netfilter_block to filter a URL

# Usage
./netfilter_block [막을 url]

# Code 분석
106~121 라인이 제일 중요 <br />

`    
	return nfq_set_verdict(qh, id, flag, 0, NULL); // flag: 1 ACCEPT, 0 DROP
`    
<br />

나머지는 기본 코드와 동일함.
