# sbt proxy 설정

conf/sbtopts에 아래 설정 추가

```
-Dhttp.proxyHost=proxy.daumkakao.io
-Dhttp.proxyPort=3128
-Dhttps.proxyHost=proxy.daumkakao.io
-Dhttps.proxyPort=3128
-Dhttp.nonProxyHosts="localhost|127.0.0.0/8|192.168.0.0/16|10.0.0.0/8|172.16.0.0/12|.daumkakao.io|.daumcorp.com|.daum.net|.kakao.com|.iwilab.com|.daumkakao.com"
```



