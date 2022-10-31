# MapReduce 기능
## GenericOptionsParser
- Hadoop job을 실행할 때 사용되는 옵션을 분석해서 configuration에 설정해주는 역할

<img src="img/GenericOptionsParser의%20Option.png" width = "300"></img>  

<span style="color:#ffd33d"> conf   </span>  
    - configuration file을 전달해서 configuration을 설정하는 옵션  
    - 다수의 속성을 한번에 설정할 때 편리함

<span style="color:#ffd33d"> D   </span>  
    - Hadoop 설정에 value 값을 추가

<span style="color:#ffd33d"> fs   </span>  
    - 지정된 uri로 기본파일시스템을 설정

<span style="color:#ffd33d"> jt   </span>  
    - 지정된 host와 port로 yarn의 리소스매니저를 설정

<span style="color:#ffd33d"> files   </span>  
    - 지정된 파일을 로컬파일시스템에서 mapreduce가 사용하는 공유 파일시스템 (주로 hdfs)으로 복사를 해서 테스크가 작업에서 사용할 수 있게 함

<span style="color:#ffd33d"> libjars  </span>  
    - 지정된 jar파일을 로컬파일시스템에서 mapreduce가 사용하는 공유 파일시스템 (주로 hdfs)으로 복사를 해서 테스크에서 클래스패스에 추가함

<span style="color:#ffd33d"> archives  </span>  
    - jar, zip, tar 파일을 맵리듀스가 사용하는 공유 파일시스템 (주로 hdfs)으로 복사를 해서 압축해제  


### Counter 
- job에 대한 통계 정보를 수집하는 기능
- 문제 진단에 유용  
        - 종류 : Built-in Counter(Task Counter, Job Counter), 사용자정의 Counter  

### 정렬
- 맵리듀스는 정렬이 기본기능
- 맵리듀스에서 제공하는 정렬과정을 이용

### Join
- 대용량 데이터셋 간의 조인을 지원
        - 종류 : Map-side Join, Reduce-side Join

### 분산캐시
- 실행시점에 파일과 아카이브의 사본을 태스크노드에 복사하여 이를 이용할 수 있게 해주는 서비스 
- -files, -archives
- API 이용(Job클래스에서 제공하는 API)

