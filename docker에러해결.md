### docker에러 발생 : docker-compose up  
- 해당 컨테이너를 restart 했을 때 에러 발생 (docker 가 정상적으로 종료되지 않아 발생한 에러)  

<img src="../img/../캡스톤디자인/img/docker에러_발생.png" width="900" height=""></img>  

### docker에러 해결방법 : 8080 포트를 사용하고 있는 pid 찾기 
- 포트가 이미 할당되어 있어서 발생한 에러로 해당 포트를 사용 중인지 확인  
<img src="../img/../캡스톤디자인/img/docker에러_pid%20찾기.png" width="400" height=""></img>  

### PID 삭제: taskkill /f /pid [삭제하고자 하는 pid]
- 할당되어 있는 포트를 죽인 후 다시 docker 컨테이너를 재시작하면 문제 해결된다.   
<img src="../img/../캡스톤디자인/img/docker에러_pid삭제.png" width="400" height=""></img>  
