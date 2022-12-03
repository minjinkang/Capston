# Spark 설치
java, python 설치되어있어야함.  
- https://dlcdn.apache.org/spark/spark-3.3.1/spark-3.3.1-bin-hadoop3.tgz 설치  
- pyspark 실행  
<img src="../img/spark_pyspark실행.png" width="500" height=""></img>  
- spark 실행 -> spark 세션을 이용해서 데이터 프레임(sample) 만들기  
<img src="../img/spark_sample.png" width="200" height=""></img>  

> transformation 실습  
- 데이터 프레임 필터링 (num이 짝수인 경우만 출력하는데 evens라는 이름으로 저장한다)  
<img src="../img/spark_sampleevens.png" width="200" height=""></img>  

> action 실습  
- 데이터 프레임 필터링(num이 짝수인 경우만 출력하는데 count룰 이용해 몇개인지 출력)  
<img src="../img/spark_samplecount.png" width="400" height=""></img>  
*위에서 설정한 1000개 중에 500개가 출력됨*  

> spark Web UI 접속  

<img src="../img/spark_webUI.png" width="500" height=""></img>  
*localhost:4040 접속*   
<img src="../img/spark_webUI확인.png" width="500" height=""></img>  
