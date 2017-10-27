---
layout: post
title: "Python Challenge prob 1"
---


#### 링크 : [http://www.pythonchallenge.com/pc/def/map.html](http://www.pythonchallenge.com/pc/def/map.html)


![](https://raw.githubusercontent.com/Rekt77/Rekt77.github.io/master/images/2017-10-27-Python_Challenge_prob_0/pyc_1_1.png)

사진을 통하여 얻어낸 데이터는 아래와 같다.

```
K -> M (ord(K)==75, ord(M)==77, K-M=2)
O -> Q (ord(O)==79, ord(Q)==81, O-Q=2)
E -> G (ord(E)==69, ord(G)==71, E-G=2)
```

데이터를 통하여 위는 [caesar cipher](https://ko.wikipedia.org/wiki/%EC%B9%B4%EC%9D%B4%EC%82%AC%EB%A5%B4_%EC%95%94%ED%98%B8)을 사용하여 문자열을 Encode 했음을 알 수 있다.

아래는 사진속 시저암호를 python 으로 decoding을 구현한 것이다.

```
g fmnc wms bgblr rpylqjyrc gr zw fylb. rfyrq ufyr amknsrcpq ypc dmp. bmgle gr gl zw fylb gq glcddgagclr ylb rfyr'q ufw rfgq rcvr gq qm jmle. sqgle qrpgle.kyicrpylq() gq pcamkkclbcb. lmu ynnjw ml rfc spj.
```

```python

#!/usr/bin/python

import string

org ='
g fmnc wms bgblr rpylqjyrc gr zw fylb. rfyrq ufyr amknsrcpq ypc dmp. bmgle gr gl zw fylb gq glcddgagclr ylb rfyr'q ufw rfgq rcvr gq qm jmle. sqgle qrpgle.kyicrpylq() gq pcamkkclbcb. lmu ynnjw ml rfc spj.'

to = 'abcdefghijklmnopqrstuvwxyz'
fr = 'cdefghijklmnopqrstuvwxyzab'
table = string.maketrans(to,fr)
result = org.translate(table)
print result

```

위의 코드를 실행하면 아래의 값이 도출된다.

```
i hope you didnt translate it by hand. thats what computers are for. doing it in by hand is inefficient and that's why this text is so long. using sring.maketrans() is recommended. now apply on the url.
```