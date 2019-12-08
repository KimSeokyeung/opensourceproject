# 더 나은 서울시 

## 프로젝트 소개
<img src="./image/intro.jpg">
#### 교통 (따릉이) / 안전(화재) 두 분야의 데이터를 사용하여
#### 데이터 분석과 시각화를 통해 서울시의 문제 현황 분석
#### 문제점 파악 후 서울시가 개선해야 할 부분 제시

## 프로젝트 페이지
#### https://kimseokyeung.github.io/opensourceproject/
2. 사용 툴
### Git : 소스코드를 효과적으로 관리하기 위해 개발된 '분산형 버전 관리 시스템’이다.

### Visual studio Code : 마이크로소프트가 마이크로소프트 윈도우, macOS, 리눅스용으로 개발한 소스 코드 편집기이다.  Python, Jupyter notenook, Git과의 연동이 가능하다.

### Tableau : 대화 형 차트, 그래프, 지도 및 앱을 만들고 공유 할 수있는 무료 BI(Business Intelligence) 도구 /  각종 데이터소스에 연결, 분석하여 대시보드, 리포트를 생산하는 분석 플랫폼이다.

Python : 고급 프로그래밍로, 플랫폼 독립적이며 인터프리터식, 객체지향적, 동적 타이핑 (dynamically typed) 대화형 언어이다.

Jupyter Notebook : 라이브 코드, 방정식, 시각화, 텍스트 등이 포함된 문서를 만들고 공유할 수 있는 오픈소스 웹 애플리케이션이다. 사용에는 데이터 청소 및 변환, 숫자 시뮬레이션, 통계 모델링, 데이터 시각화, 기계 학습 등이 포함된다.

NumPy : NumPy는 Numerical Python의 줄임말로 고성능 과학 컴퓨팅과 데이터 분석에 필요한 기본 패키지다. NumPy는 데이터 분석에서 거의 모든 상위 레벨의 도구가 만들어지는 기반이다. 

Pandas : Pandas는 Python에서 빠르고 쉽게 데이터 분석을 할 수 있도록 고안된 고도의 데이터 구조와 조작 도구가 들어 있는 주요 패키지이다. Pandas는 NumPy 위에 세워져 있고 NumPy 중심 어플리케이션에서 쉽게 사용할 수 있다. 

GeoPandas : GeoPandas는 파이썬에서 지리정보 데이터 처리의 기하하적 연산과 시각화 등을 돕는 패키지이다.

Atom : Free-Open source 형태의 리눅스, 윈도용 문서 및 다양한 프로그래밍 언어의 편집기이다.

QGIS : 데이터 뷰, 편집, 분석을 제공하는 크로스 플랫폼 Free - Open source 데스크톱 지리 정보 체계(GIS) 응용 프로그램이다.

JSON : JavaScript Object Notation (JSON)은 Javascript 객체 문법으로 구조화된 데이터를 표현하기 위한 문자 기반의 표준 포맷이다.

REQUESTS : Apache2 라이센스에 따라 릴리스 된 Python HTTP 라이브러리이다. 이 프로젝트의 목표는 HTTP 요청을 더 단순화는 것으로, Open API loding시 사용 된다.

3. 계획 완성도
3-1. 따릉이(100%)
따릉이 실시간 API를 사용
-  대여소 별 거치대 수, 자전거 수 등 정보 제공
-  사용자가 원하는 특정 구역 필터링 기능 제공 
     ex) 지하철역, 대학교, 자치구 등

따릉이 공공데이터 사용
-  시간대,요일별 이용량 통계
-   효율적인 자전거 재배치를 위한 분석 제공
-  대여소를 기준으로 한 자전거 이동 패턴 분석
*분석결과 요일보다 시간대별 상관관계가 유의미하여, 시간대별 이용량 통계에 집중함   

3-2. 화재위험 감소방안 분석(100%)
화재발생과 관련지을 수 있는 다양한 데이터를 사용하여 분석
1 - A  화재의 원인과 가장 큰 원인이 된 것이 무엇인지 파악 
1 - B  어느 지역에서 화재가 발생했는지 분석 
1 - C 무엇이 원인이 되어 얼마만큼의 화재 수가 발생했는지 파악

소방서 및 소방시설 위치와 현황, 화재 사고 데이터와 접목시켜 현 상황에서의 문제점 파악

분석한 데이터를 바탕으로 소방시설 부족 구역의 설치 추천 및 안전 취약지역 감지



4. 코드 및 사용 데이터
4-1. 교통(따릉이) 

4-1-1. 실시간 따릉이 현황 및 시계열 분석
	[코드]
Bicycle_Time_series_analysis.ipynb : 따릉이 자전거 대여소 별 시계열 분석 코드

[사용 데이터]
서울특별시  공공자전거 실시간 대여정보 API : 실시간 따릉이별 거치대 거치율 정보
http://openapi.seoul.go.kr:8088/5058644a58646c733132324e6448695/json/bikeList/1/1000
http://openapi.seoul.go.kr:8088/5058644a58646c733132324e6448695/json/bikeList/1001/2000

using_No.csv : 분석에 사용할 따릉이 거치대 번호
data_in_.csv : 시계열 분석으로 나온 시간대 별 반납 이용량  분석 결과
data_out_.csv : 시계열 분석으로 나온 시간대 별 대여 이용량 분석 결과
data_in.csv : 위 데이터를 시각화 툴에 맞는 형태로 바꾼 데이터
data_out_.csv : 위 데이터를 시각화 툴에 맞는 형태로 바꾼 데이터
서울특별시 공공자전거 대여정보_201901.csv : 따릉이 2019년 01월 사용 통계 파일
서울특별시 공공자전거 대여정보_201902.csv : 따릉이 2019년 02월 사용 통계 파일
서울특별시 공공자전거 대여정보_201903.csv : 따릉이 2019년 03월 사용 통계 파일
서울특별시 공공자전거 대여정보_201904.csv : 따릉이 2019년 04월 사용 통계 파일
서울특별시 공공자전거 대여정보_201905.csv : 따릉이 2019년 05월 사용 통계 파일

*대용량 데이터(100MB 이상)는 git에 upload가 불가능하여 google cloud에 upload
[따릉이분석 사용 데이터 파일] 
https://drive.google.com/drive/folders/1bw3jGen8kC6ueqafPqyaRSTS3QtVU4Df?usp=sharing


	[코드]
Bicycle_in&out_analyze.ipynb : 따릉이 자전거 대여소 별 실시간 상황 분석 및 
   좌표값, 추가 정보 병합 코드

	[사용 데이터]

서울특별시  공공자전거 실시간 대여정보 API : 실시간 따릉이별 거치대 거치율 정보
http://openapi.seoul.go.kr:8088/5058644a58646c733132324e6448695/json/bikeList/1/1000
http://openapi.seoul.go.kr:8088/5058644a58646c733132324e6448695/json/bikeList/1001/2000

using_No.csv : 분석에 사용할 따릉이 거치대 번호
data_in.csv : 시계열 분석으로 나온 시간대 별 반납 이용량  분석 결과
data_out.csv : 시계열 분석으로 나온 시간대 별 대여 이용량 분석 결과
공공자전거 대여소 정보_201905.csv : 5월까지 등록된 거치대 정보 
final_out : 각 거치대별 시계열 분석 정보 및 기존 좌표정보, 현재 거치 상황에 대한 데이터

*대용량 데이터(100MB 이상)는 git에 upload가 불가능하여 google cloud에 upload
[따릉이분석 사용 데이터 파일] 
https://drive.google.com/drive/folders/1bw3jGen8kC6ueqafPqyaRSTS3QtVU4Df?usp=sharing

4-1-2. 따릉이 경로 분석
	[코드]
	merge_bicycle.ipynb : 1-5월 사용 경로 정보 전처리 코드
	Destination_analyze.ipynb

	[사용 데이터]
	bicycle.csv : 1월 ~ 5월사이에 있던 사용 경로 정보
using_No.csv : 분석에 사용할 따릉이 거치대 번호
	공공자전거 대여소 정보_201905.csv : 5월까지 등록된 거치대 정보
	path.csv : 시각화 툴에 맞춘 사용 경로 정보
	path_count.csv : 사용 경로 별 이용 횟수 정보
name.csv : 대여소 번호 별 대여소 명 정보 
서울특별시 공공자전거 대여정보_201901.csv : 따릉이 2019년 01월 사용 통계 파일
서울특별시 공공자전거 대여정보_201902.csv : 따릉이 2019년 02월 사용 통계 파일
서울특별시 공공자전거 대여정보_201903.csv : 따릉이 2019년 03월 사용 통계 파일
서울특별시 공공자전거 대여정보_201904.csv : 따릉이 2019년 04월 사용 통계 파일
서울특별시 공공자전거 대여정보_201905.csv : 따릉이 2019년 05월 사용 통계 파일

*대용량 데이터(100MB 이상)는 git에 upload가 불가능하여 google cloud에 upload
[따릉이분석 사용 데이터 파일] 
https://drive.google.com/drive/folders/1bw3jGen8kC6ueqafPqyaRSTS3QtVU4Df?usp=sharing


4-1-3. 따릉이 재배치
	[코드]
Bicycle_system_ optimization&Reframing_data.ipynb : 따릉이 재배치 경로 지정 코드

[사용 데이터]
서울특별시  공공자전거 실시간 대여정보 API : 실시간 따릉이별 거치대 거치율 정보
http://openapi.seoul.go.kr:8088/5058644a58646c733132324e6448695/json/bikeList/1/1000
http://openapi.seoul.go.kr:8088/5058644a58646c733132324e6448695/json/bikeList/1001/2000

bicycle.csv : 1월 ~ 5월사이에 있던 사용 경로 정보
using_No.csv : 분석에 사용할 따릉이 거치대 번호
	공공자전거 대여소 정보_201905.csv : 5월까지 등록된 거치대 정보 
	move.csv : 재배치 경로 및 재배치 양에 대한 정보
	optimize_path.csv : 시각화 툴에 맞춘 재배치 경로 및 재배치 양에 대한 정보

*대용량 데이터(100MB 이상)는 git에 upload가 불가능하여 google cloud에 upload
[따릉이분석 사용 데이터 파일] 
https://drive.google.com/drive/folders/1bw3jGen8kC6ueqafPqyaRSTS3QtVU4Df?usp=sharing 





4-2. 안전(화재)

4-2-1. 자치구 별 '화재 발생 횟수' 대비 소방시설, 소방인력수, 장비의 수 비교
	[코드]
	fire_relocation.ipynb : 자치구 별 '화재 발생 횟수' 대비 소방시설, 소방인력수, 
장비의 수 분석 코드
          
	[사용 데이터]
	전국 소방서 현황(2018.11.28).csv : 전국 소방서 정보 
	전국 119안전센터 현황(2018.11.28).csv : 전국 119안전센터 정보 
서울시 소방 공무원 (정원) 통계.csv : 소방소 별 소방 공무원 수
서울시 행정구역 시군구 정보 (좌표계_ WGS1984).csv : 서울시 자치구 별 위치 
서울시 화재발생 현황(구별)통계 : 자치구 별 화재 발생 평균
fire_gu_col.csv : 자치구 별 화재 통계
fire_jangbi.csv : 소방서 별 장비 보유 대수
df_firesafe.csv : 서울 내 소방서, 119 안전센터 위치(위도,경도)
test_all.csv : ‘자치구 별 '화재 발생 횟수' 대비 소방시설, 소방인력수, 장비 수

4-2-2. 화재발생 원인 분석
[코드]
fire_cause.ipynb : 화재 발생 원인 전처리 코드

[사용 데이터]
fire_cause.csv : 화재 발생 원인 데이터
gu_long_lat.csv : 자치구별 중심 좌표
df_cause.csv: 전처리 완료한 화재 발생 원인 데이터
	
*대용량 데이터(100MB 이상)는 git에 upload가 불가능하여 google cloud에 upload
[화재 취약지역 분석 seoul.shp 파일] 
https://drive.google.com/drive/folders/1_iE_MgjzaqWf7nhmS-BkPsNVB54ywSi6?usp=sharing

4-2-3. 화재 취약지역
	[코드]
fire_area.ipynb : 데이터 전처리 코드

[사용 데이터]
firesafe.csv : 소방서 및 안전센터 위치
sigungu.csv : 자치구별 중심 좌표
street.csv : 도로 위치
df_area.csv : 화재 취약지역 좌표 (서소위치/도로/노후/스프링쿨러/외장재) 






4-3. 최종 시각화
	
4-3-1. 교통따릉이
	Bicycle_system_1.html : 실시간 따릉이 현황 및 시계열 분석
    -> 반납 및 대여 현황 시각화 
Bicycle_system_2.html : 따릉이 경로 분석 시각화
Bicycle_system_3.html : 따릉이 전체 재배치 경로 및 세분화 시각화

4-3-2. 안전(화재)
fire_1.html : 서울시 화재 발생 원인 시각화
fire_2.html : 자치구 별 화재 발생 횟수 시각화
fire_3.html : 자치구 별 화재 발생 원인 시각화
fire_area.html : 화재 취약지역 시각화 
fire_5.html :  ‘자치구 별 '화재 발생 횟수' 대비 소방시설, 소방인력수, 장비 수 시각화
fire_6.html : 상위 4개 취약 자치구 시각화 


5. 기여도
변준영 - 따릉이 전체 분석 및 시각화 (30%)
윤혜정 - 화재발생 원인 분석 및 시각화 (23%)
김서경 -  자치구 별 '화재 발생 횟수' 대비 소방시설, 소방인력수, 장비의 수 분석 및 시각화 / git page 연동 (23%) 
이정은 - 화재 취약지역 분석 및 시각화 / 따릉이 경로 분석 파일 전처리 (24%)


6. Commit 내역
캡쳐해서 넣기~!~!~!


7. git / git page 주소
git : https://github.com/KimSeokyeung/opensourceproject
git page : https://kimseokyeung.github.io/opensourceproject/
