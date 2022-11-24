# Kafka 설치  
**Doker 환경에서 클러스터를 구축함*  
## docker-compose.yml 파일 작성과 kafka 클러스터 실행  
<span style="color:red">*주키퍼 설치를 위한 코드*</span>  
<img src="../img/kafka_docker-compose_zookeeper.png" width="200" height=""></img>  
<span style="color:#ffd33d">*주키퍼 설치, 실행 확인*</span>  
<img src="../img/kafka_docker-compose_zookeeper실행.png" width="200" height=""></img>  
<img src="../img/kafka_docker-compose_zookeeper실행확인.png" width="300" height=""></img>  
<span style="color:red">*kafka 클러스터를 구축하기 위한 코드 (broker1, broker2, broker3)*</span>  
<img src="../img/kafka_docker-compose_broker1.png" width="600" height=""></img>  
<img src="../img/kafka_docker-compose_broker2.png" width="600" height=""></img>  
<img src="../img/kafka_docker-compose_broker3.png" width="600" height=""></img>  
<span style="color:#ffd33d">*주키퍼 실행 중단*</span>  
<img src="../img/kafka_docker-compose_zookeeper실행기록삭제.png" width="200" height=""></img>  
<span style="color:#ffd33d">*주키퍼 실행(docker-compose up)과 동시에 broker1,2,3 실행*</span>  
<img src="../img/kafka_docker-compose_broker실행.png" width="400" height=""></img>  
<span style="color:#ffd33d">*주키퍼, broker 실행 확인*</span>  
<img src="../img/kafka_docker-compose_broker실행확인.png" width="300" height=""></img>  
<span style="color:red">*kafka 클러스터를 위한 webUI 코드*</span>  
<img src="../img/kafka_docker-compose_webui.png" width="250" height=""></img>  
<span style="color:#ffd33d">*전체 실행(docker-compose up)*</span>  
<img src="../img/kafka_docker-compose_webui실행.png" width="500" height=""></img>  
<span style="color:#ffd33d">* kafdrop에 접속하여(localhost:8080) 전체 실행 확인*</span>  
<img src="../img/kafka_docker-compose_webui실행확인.png" width="400" height=""></img>  

