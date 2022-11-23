# HDFS JAVA API 실습 (1)
## 1. hadoop 클러스터 구동
- hdfs namenode -format  
cd sbin  
start-dfs.cmd  
start-yarn.cmd 

** jps : jps명령어는 실행중인 JVM(Java virtual Machine) 프로세스 상태를 보여주는 것  
<img src="../img/jps.png" height="100">

## 2. maven 설치
    - apache-maven-3.8.6
    -  maven home 환경변수 설정 


## 3. mvn package 실행  
<img src="../img/mvn%20package.png" width="400" height="300">

    1. hdfs-example에 있는 폼파일을 hdfs에 업로드하기
<img src="../img/user-fastcampus만들기.png" width="400" height="">

<img src="../img/user생성된거확인하고%20폼파일%20올리기.png" width="400" height="">

<img src="../img/폼파일업로드확인.png" width="600" height="55">

    2. 업로드한 폼파일을 vscode에서 실행해서 출력하기

<img src="../img/FileSystemPrint.png" width="500" height="300">

<img src="../img/폼파일출력.png" width="400" height="300">

<span style="color:#ffdce0">*hadoop jar 명령어를 이용하여 실행(타켓에 hdfs 자르파일 입력 + 실행할 메인 클래스위치를 지정 + hdfs에 위치하는 args를 넣고 실행) => 하둡파일시스템으로부터 읽어서 출력* </span>  


# HDFS JAVA API 실습 (2)
## <span style="color: #ffd33d">디렉토리 목록을 조회</span>

    1. 빌드  
<img src="../img/ListStatus.png" width="600" height="300">
<img src="../img/ListStatusmvn빌드.png" width="400" height="300">

    2. 실행
<span style="color:#ffdce0">*hadoop jar 명령어를 이용해 실행 + com.fastcampus.hadoop.ListStatus (실행할 메인함수와 위치를 알려줌) + 인풋아규먼트로 /user/fastcampus 위치의 리스트 목록을 받아옴*</span>

<img src="../img/3해당위치의%20디렉토리목록을%20받아옴.png" width="800" height="">

<img src="../img/4%20fs-ls%20명령어이용.png" width="600" height="">

## <span style="color: #ffd33d">로컬에 있는 파일을 hdfs에 복사</span>
<span style="color:#ffdce0">*= CLI로 CopyFromLocal, Put 명령어와 같음*</span>

    1. 빌드
<img src="../img/copyFromLocal.png" width="600" height="300">
<img src="../img/CopyFromLocalmvn빌드.png" width="400" height="">

    2. 실행 
<span style="color:#ffdce0">*파일 뭐있는지 확인하고 삭제*</span>  
<img src="../img/pom.xml파일삭제.png" width="600" height="">

<span style="color:#ffdce0">*hadoop jar 명령어를 이용 / 실행할 메인 함수가 있는 클래스 지정 / [첫번째 인자 소스를 주고] + [두번째 인자 user/fastcampus/pom.xml (pom.xml을 복사하겠다! 복사할 파일명까지 작성)]*</span>
<img src="../img/copyFromLocal%20명령어javaapi.png" width="600" height="">

<img src="../img/copyFromLocal%20명령어%20업로드%20확인javaapi.png" width="600" height="">

<span style="color:#ffdce0">*해당파일이 제대로 복사가 되었는지 확인 cat*</span>  
<img src="../img/cat%20javaapi.png" width="600" height="">

## <span style="color: #ffd33d">로컬에 있는 파일삭제</span>

    1. 빌드
<img src="../img/DeleteFilejavaapi.png" width="600" height="300">
<img src="../img/DeleteFilemvn빌드.png" width="400" height="">

    2. 실행 
<span style="color:#ffdce0">*hadoop jar 명령어를 이용 / 실행할 메인 함수가 있는 클래스 지정 / [첫번째 인자 소스 : 삭제할 파일 위치와 파일]*</span>  
<img src="../img/DeleteFile명령어javaapi.png" width="600" height="">

