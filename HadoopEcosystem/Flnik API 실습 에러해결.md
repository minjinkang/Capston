[현상]  
자바 프로그램을 동작시켰더니 아래와 같은 WARN이 발생

log4j:WARN No appenders could be found for logger (org.apache.cayenne.conf.DefaultConfiguration).
log4j:WARN Please initialize the log4j system properly.

[원인]  
log4j 라는 모듈의 설정의 문제이다.

[해결방법]
(https://www.jami.name/205)  
log4j.properties를 java프로젝트 src파일에 넣어준다.
