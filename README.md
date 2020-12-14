# dbp_final

------------
+ 홈페이지 링크
>
> http://swinfo.dothome.co.kr/
------------
+ 주제선정이유 / 프로젝트 목적

> 대부분의 사람들이 교통수단으로 지하철을 애용합니다. 하지만 지하철 이용 시에 불편했던 부분들이 있습니다. 예를 들면 짐이 너무 많아 짐을 물품 보관함에 맞기고 싶은데 물품 보관함이 어디 있는지 모르는 상황이 발생하는 것입니다. 따라서 지하철 이용 시 가장 불편했던 점 세 가지를 뽑아 웹페이지를 만들게 되었습니다. 저희가 고른 3가지는 첫 번째, 특정 역의 승하차 인원입니다. 어제는 지하철 안에 사람이 많지 않아서 앉아서 갔지만, 오늘은 시간대를 잘못 선택하여 계속 서서 가는 불편함을 종종 겪습니다. 따라서 승하차 인원을 확인하고 어떤 시간대가 가장 붐비는지, 여유로운지를 알면 서서 가는 불편함을 줄일 수 있습니다. 두 번째는 지하철의 엘리베이터 정보입니다. 몸이 불편하거나 큰 짐이 있어 계단을 이용하지 못할 경우에 엘리베이터를 이용해야 합니다. 특정 역에서 엘리베이터가 어디에 있는지를 검색으로 알 수 있다면 보다 편리하게 엘리베이터를 이용할 수 있을 것입니다. 마지막으로는 물품 보관함의 위치입니다. 우리는 무거운 짐을 가지고 있거나 피치 못할 사정으로 소지품을 가지고 다니지 못할 경우에 물품 보관함을 이용합니다. 이때 물품 보관함의 위치를 알 수 있다면 보다 빠르고 쉽게 물품 보관함을 이용할 수 있습니다. 이에 따라 조금 더 편리한 지하철 이용을 위하여 저희는 특정 역의 승하차 인원, 엘리베이터 정보, 그리고 물품 보관함의 정보가 나오는 웹페이지를 만들기로 하였습니다.
------------
+ 구축환경 정보

> 호스팅 - Dothome
> 데이터베이스 - mySQL, phpMyAdmin   
> 사용 언어 - PHP, HTML, CSS
------------
+ 데이터 출처

> 1. 특정 역에서 어떤 시간대에 가장 승하차 인원이 많은지, 가장 적은지   
> http://data.seoul.go.kr/dataList/OA-12252/S/1/datasetView.do

> 2. 지하철역 엘리베이터 정보   
> https://www.data.go.kr/data/15044261/fileData.do

> 3. 지하철역 물품 보관함 정보   
> https://www.data.go.kr/data/15044234/fileData.do
------------
+ 데이터베이스
> DB) Subway
	- 승하차별 인원수 : time
	- 물품보관함 : locker
	- 엘리베이터 : elevator
  
> 컬럼명)
    time))
    - 월별: month
    - 호선: line
    - 역명: station
    - 승차시간: rtime0_0  예))rtime4_5, rtime5_6
    - 하차시간: qtime0_0  예))qtime4_5, qtime5_6
    
    locker)
    - 호선: line
    - 역명: station
    - 위치: l_location
    
  
    elevator
     - 호선: line
    - 역명: station
    - 내, 외부 여부: e_num
    - 엘리베이터 설치위치: e_location
 ------------
 + 홈페이지 
 http://swinfo.dothome.co.kr/
 ------------
    
+ 홈페이지 소개

> * 메인화면   
![메인](https://user-images.githubusercontent.com/70924137/102069648-64cec180-3e41-11eb-83c5-5db139e4c606.JPG)

>메인화면은 승하차 정보를 알 수있는 Population, 물품보관함 정보를 알수 있는 Locker, 엘리베이터 정보를 알 수 있는 Elevator, 그리고 기타 정보들이 나오는 Others페이지로 넘어 갈 수 있는 페이지입니다. 각각의 페이지는 Line(지하철 호선)을 클릭해 넘어갈 수 있습니다. 또한 현재 시간과 온도를 알 수 있으며 지하철 느낌의 bgm도 삽입하였습니다.

> * Population   
![population](https://user-images.githubusercontent.com/70924137/102070601-ac098200-3e42-11eb-8c79-e493b2481d3c.JPG)

> Line(호선) 클릭을 통해 넘어간 Poplulation 페이지는 승차/하차로 나눠져 역명을 검색할 수 있습니다.   
> 역명을 검색하면 검색역명의 승차 혹은 하차 인원수를 달별(2020년 1년간), 시간별로 볼 수 있습니다.

> * Locker

![Locker](https://user-images.githubusercontent.com/70924137/102070867-0f93af80-3e43-11eb-9049-206435985987.JPG)

>Line(호선) 클릭을 통해 Locker 페이지로 넘어가면 다시 역명을 검색하는 페이지가 나옵니다.   
>역명을 검색하는 페이지에서 역명을 검색하면 해당 역의 물품보관함 정보를 볼 수 있습니다.

> * Elevator

![Elevator](https://user-images.githubusercontent.com/70924137/102071136-68fbde80-3e43-11eb-91ad-18bee0753009.JPG)

> Line(호선) 클릭을 통해 Elevator 페이지로 넘어가면 다시 역명을 검색하는 페이지가 나옵니다.   
> 역명을 검색하는 페이지에서 역명을 검색하면 해당 역의 엘리베이터 정보를 볼 수 있습니다.

> * Others

![Others](https://user-images.githubusercontent.com/70924137/102071402-c5f79480-3e43-11eb-9ff4-0d8d348360fc.JPG)

> 메인페이지에서 Others섹션의 Click을 클릭하면 시간, 날짜, 지하철노선도, 뉴스, SNS정보등 여러가지 기타 정보들을 얻을 수 있습니다.
------------
+  역할분담

> 프론트 - 박민지, 이지원   
> 백 - 김현성, 서태민, 이은영   
------------
+ 프로젝트 개선점
> 메인페이지에서 other 세션을 활용해서 시간, 날짜, 지하철 노선도 등 여러가지 다양한 정보를 얻을 수 있도록 하였다.   
  무료 호스팅 서비스를 이용해서 직접 웹서버를 구축하지 않고 소규모 웹페이지를 만들 수 있었다.  
  사용자가 해당 역을 검색해서 엘리베이터의 상세한 위치 정보와 물품 보관함의 상세한 위치 정보를 얻을 수 있도록 하였다.  
------------
+ 느낀점
> 한학기 동안 배운 내용을 복습할 수 있는 좋은 기회였다.      
  팀원들과 같이 상의해서 구현하고 싶은 웹사이트도 만들고 협업 능력도 기를 수 있는 소중한 경험을 하였다.    
  팀원 모두 적극적으로 참여해 유의미한 결과를 만들어내서 매우 뿌듯하다.    
------------
+ 참고 문헌
>  데이터 수집 : https://www.data.go.kr/      
   백엔드  : https://webseodang.tistory.com/159  
 




