# Flink DataStream API 실습  
- 사람 클래스에 대한 일련의 레코드를 입력으로 받아 그 중에 '성인'만을 필터링하는 실습  
1. mvn project 생성  
   - maven-archetype-quickstart > v.1.4 > 그룹id : com.fastcammpus.flink > flink-example > 경로설정    
   - version : 1.0.0  

2. pom.xml 편집  
    - build, junit 삭제  
    - properties : 자바버전 1.8 변경  // flink 버전 1.15.0
    - dependencies : flink dependency 파일 추가  
<img src="../img/flink실습_DataStream%20pom파일편집.png" width="400" height=""></img>  

3. 소스코드 작성 (DataStreamExample.java)  
<img src="../img/flink실습_DataStream%20java.png" width="400" height=""></img>  

4. flink 클러스터에 job 제출  
   1. mvn package  
<img src="../img/flink실습_DataStream%20java%20mvn%20package.png" width="400" height=""></img>  
   2. 클러스터에 제출  
<img src="../img/flink실습_DataStream%20클러스터제출.png" width="400" height=""></img>  
   3. localhost:8081 flink 대쉬보드 > TaskManagers > Stdout 에서 확인가능  
<img src="../img/flink실습_DataStream%20로컬호스트에서확인.png" width="400" height=""></img>  

5. 로컬에서 실행하는 방법  
- java run   
<img src="../img/flink실습_DataStream%20로컬에서%20실행.png" width="400" height=""></img>  
