# Flume 실습1

     apache-flume 다운, 압축해제, 시스템환경변수편집  
<img src="../img/시스템환경변수편집1.png" width="300" height=""></img>  
<img src="../img/시스템환경변수편집2.png" width="250" height=""></img>  

    flume 설정파일 만들기 - example.conf  
<img src="../img/flume설정파일exampleconf.png" width="300" height=""></img>  

    Flume agent 실행  
<img src="../img/flume%20example.conf%20실행.png" width="500" height=""></img>  
<span style="color:#ffd33d">*flume-ng agent -n a1 -c conf -f example.conf -property flume.root.logger=Debug,console*</span>  

    telenet 실행  
<img src="../img/telnet%20실행.png" width="300" height=""></img>  

    netcat 실행결과  
<img src="../img/netcat%20실행결과.png" width="900" height="40"></img>  


# Flume 실습2

    하둡클러스터 작동
<img src="../img/jps%20확인.png" width="400" height=""></img>  

    설정파일 생성
<img src="../img/flume실습2설정파일%20target.png" width="500" height=""></img>  

<img src="../img/flume실습2설정파일%20source.png" width="500" height=""></img>  
- *target_agent의 이름 AvoroIn*  
- <span style="color:#ffd33d">*채널이 두개인 이유는 hdfs와 로컬에 저장할 것이기 때문에 Sink가 2개 필요 = 메모리 채널도 2개*</span>  
- *rollSize = 0 파일크기에 제한을 두지 않음* 
- *rollCount = 10000 log가 10000개 이상 기록되면 rolling 할 것*  
- *rollInterval = 600 600초가 지날 때마다 rolling 할 것*  

        Sink Directory 생성
<img src="../img/flume디렉터리생성hdfs.png" width="800" height=""></img>  

        Flume agent
1. target agent 실행
<img src="../img/flumetarget실행.png" width="900" height=""></img>  
2. source agent 실행
<img src="../img/flumesource실행.png" width="900" height=""></img>  
<img src="../img/flumesource실행오류.png" width="900" height=""></img>  
<span style="color:#ffd33d">*source.conf 파일이 실행은 되지만 리눅스 tail -f 명령어는 윈도우 커맨드에서 사용이 불가하기때문에 오류가 생긴다// 해결방법을 찾지 못하였다.*</span>  

        실행결과
<img src="../img/flumesource실행정상로그.png" width="900" height="400"></img>  

<span style="color:#ffd33d">*리눅스 tail -f 명령어는 log를 실시간으로 계속 보여줄 수 있는 기능이다.*</span>