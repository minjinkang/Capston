# MapReduce 기능 WordCountWithCounter 실습
> WordCount 실습에 Counter 사용
1. WordCountWithCounter.java 파일작성

<span style="color:#ffd33d">*앞서 작성한 WordCoutn.java와 리듀서, 드라이버는 같은 코드이다.*</span>  
<img src="img/java%20wordcountwithcounter%20.png" width="600" height="400"></img> 

2. WordCountWithCounter 실행

<img src="img/java%20wordcountwithcounter%20실행.png" width="600" height=""></img>  
<span style="color:#ffd33d">*output2 디렉터리에 실행결과 저장*</span>  
<span style="color:#008000">*hadoop jar .\target\mapreduce-example-1.0.0.jar : jar명령어*</span>  
<span style="color:#008000">*com.fastcampus.hadoop.WordCountWithCounter : 함수가 존재하는 클래스 파일경로*</span>    
<span style="color:#008000">*/user/fastcampus/LICENSE.txt : input 경로에 input파일 생성*</span>  
<span style="color:#008000">*/user/fastcampus/output2 : output2경로에 output파일 생성*</span>  

3. WordCountWithCounter  결과

<img src="img/java%20wordcountwithcounter%20실행%20결과.png"></img>  
<span style="color:#ffd33d">*결과 : 특수문자가 포함되지않은 글자수 = 1672*</span>

