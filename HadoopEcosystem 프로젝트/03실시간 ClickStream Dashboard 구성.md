# 실시간 Dashboard  
- Grafana를 이용하여 실시간 클릭스트림 통계 정보를 통합하여 시각화한다.  
<img src="../img/실시간대시보드.png" width="400" height=""></img>  

> Grafana 실행  

<img src="../img/grafana실행.png" width="400" height=""></img>  
    - localhost:3000 접속  (초기 아이디, 비번 : admin)  
<img src="../img/grafana_접속.png" width="400" height=""></img>  

1. Log Generator - main.java 실행 : 실제 로그들이 kafka topic으로 전송한다.
2. clickstream_clickstreamanalyzer자바실행 : 로그 정보를 kafka로부터 가져와서 분석결과를 처리해준다. 결과는 mysql DB에 저장된다.   
<img src="../img/grafana_자바파일%20실행.png" width="400" height=""></img>  

3. Grafana에서 대쉬보드 생성
    - grafana 내에서 mysql에 있는 데이터베이스로부터 데이터를 가져오기위한 데이터소스를 생성한다.  
*Configration > Data source*  
<img src="../img/grafana_mysqldatasource.png" width="400" height=""></img>  
<img src="../img/grafana_mysqldatasource정보입력.png" width="400" height=""></img>  

    - 대쉬보드 생성  
*Dashboards > New dashboard*  
<img src="../img/grafana_new대쉬보드생성.png" width="400" height=""></img>  
    - <span style="color:#ffd33d">*mysql로부터 데이터를 읽는 형대로 패널 구성한다. -->   *하단에 쿼리정보를 입력하여 저장**</span>  
<img src="../img/grafana_acrivesessioncount패널.png" width="600" height=""></img>  
<img src="../img/grafana_adspersecond패널.png" width="600" height=""></img>  
<img src="../img/grafana_requestpersecond패널.png" width="600" height=""></img>  
<img src="../img/grafana_errorpersecond패널.png" width="600" height=""></img>  

4. 패널 전체 확인  
<img src="../img/grafana_4패널.png" width="600" height=""></img>  

5. 실시간 스트림 패널 확인  
<img src="../img/grafana_실시간확인1.png" width="600" height=""></img>  
<img src="../img/grafana_실시간확인2.png" width="600" height=""></img>  












