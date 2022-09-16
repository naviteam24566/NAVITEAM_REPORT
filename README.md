<h1 align="center"> 2022 SW Education for Vietnamese Students in Korea </h1>

![alt](https://user-images.githubusercontent.com/112414846/188490124-e460e3f9-04e0-44cb-b1a4-b4e32a8651f0.png)

<h1 align="center"> TEAM PROJECT REPORT </h1>

<h2 align="center"> 유기동물보호 관리시스템 연구 </h2>

### **Author**: Navi Team <br>
Email: naviteam24566@gmail.com
   
| 팀원     | 이메일 | 전화번호 | 역할 |
|:---------:|:----------:|:----------:|:----------:|
| 황반콰  | hoangkhoa21913388@gmail.com | 010 - 2388 - 1398 | 보고서,PPT 작성 및 웹사이트 |
| 황티타오 | hoangthao21921541@gmail.com | 010 - 5788 -1398 | 보고서 작성 및  웹사이트 |
| 팜티궤느  | phamthiquenhu.inu@gmail.com | 010 - 4472 -1095 | 데이터, 프로그램 처리 및 분석|
| 도트엉동 | truongdong.sju@gamil.com | 010 - 9751 -9606 | 프로그램 작성 및 debug |
| 반광틴 | quangthinh.276@gmail.com | 010 - 2800 -2767 |  ChatBot, 프로그램 처리 |

   

<h3 align="left"> I. 유기동물 개념 및 현황 </h3>
<h4 align="left"> 1. 유기동물 개념  </h4>

   유기동물 (영어: abandoned pets)은 주인의 실수, 혹은 의도적인 목적으로 인하여 버려진 이국적인 동물, 혹은 반려동물을 뜻한다.  <br>
 이 동물들은 음식과 물이 없어 죽는 경우가 많지만, 운이 좋은 경우 부동산 업자와 은행 사무관의 차압과정에서 발견되기도 한다.
 
 <h4 align="left"> 2. 유기동물 현황  </h4>
 
 * 대한민국에서는 2011년 기준 매년 8만 여 마리의 반려동물이 버려지는 것으로 집계된다.
 * 버려지는 반려동물이 매년 10만 여 마리에 달한다는 의견도 있다.
 * 유기동물의 전년대비 증가율은 16년 9.3%, 17년 14.4%, 18년 17.9%를 기록하였다.
 * 유기동물이 늘어나면서 구조·보호 비용을 포함한 운영비도 많이 늘어났다. 
 * 2018년 동물보호센터 운영비는 전년의 155억 5000만원에 비해 28.9%가 증가한 200억 4000만원이 소요되었다.
 
 <h4 align="left"> 3. 유기동물 원인  </h4>
 
 동물들은 다양한 이유로 인해 유기된다:
 * 예쁘고 귀엽다는 이유로 입양했다가 나중에 늙고 병들어 동물의 외모가 마음에 들지 않거나 많이 다쳐서 치료비가 부담들어서 등, 다양한 명분을 들며 반려동물을 유기한다.
 * 주인이 동물의 행동과 심리를 이해하지 못해서 생긴 갈등 때문에 유기하는 경우도 있다.
 * 유기동물들은 주로 주인의 죽음이나, 혹은 동물들이 너무 커지거나 질병에 걸린 경우 발생한다.



<left><img width="350" height="200" src="https://cdn.mground.kr/mground/2021/11/%EC%95%88%EB%9D%BD%EC%82%AC%EC%9C%84%EA%B8%B0-%EC%9C%A0%EA%B8%B0%EA%B2%AC-%EC%9E%85%EC%96%91.jpg"><left>
<img width="300" height="200" src="https://image.kmib.co.kr/online_image/2020/0729/611718110014851798_1.jpg" />
<img width="350" height="200" src="https://img.animalplanet.co.kr/thumbnail/2020/07/23/2000/8s6nt1hl1016wh1l06br.jpg" />
 

   * 이상으로 유기동물의 현황에 의하여 한국 정부는 동물소유자의 사육·관리 의무를 강화하고 동물 학대 등 위법행위시 처벌 규정 또한 대폭 강화함으로써 2008년 1월 27일부터 개정된 동물보호법이 시행되고 있다. 
   
   * 현재, 동물보호를 하는 것도 사회적인 많은 관심을 받는 문제이다. 
   
   * 우리 팀도 유기동물뿐만 아니라 모든 동물을 보호하기 위해서 도워주고 싶기 때문에 **유기동물의 정보를 관리하고자 웹사이트**를 개발하기로 했다. 또한 **"CHATBOT"** 성능을 활용하여 이메일이나 문자로 유기동물의 정보를 받을 수 있을 것이다.
   
 <h3 align="left"> II. 데이터 처리 및 분석 </h3>
 We conduct getting data in 2 methods:
 - Method 1: Use open API to download data by xml format, import data manually
 - Method 2: Use code to download data to file and import these data into MySQL automatically. Here, we use logstash to bring data from MySQL into Kibana
 
<h4 align="left"> 1. 진행 방식  </h4>
 
* Open data를 가져오기.
* 데이터를 수정 및 import 하기.
* 인덱스 매핑 및 템플릿을 이용하고 인덱스 생성.
* 키바나를 통해서 시각화하기 (잠고: 엘라스틱서치, 키바나, 러그스태스를 설치하고 실행한다)
 
 <h4 align="left"> 2. 데이터 를 가져 오기  </h4>
   
* 공공데이터 Open API 활용하여 CSV파일을 가져온다. [전국동물보호센터정보표준데이터](https://www.data.go.kr/tcs/dss/selectApiDataDetailView.do?publicDataPk=15025454)
* 동물보호관리시스템 유기동물 조회 서비스: [공공데이터 URL](https://www.data.go.kr/data/15098931/openapi.do) 
   (농림축산식품부 농림축산검역본부_동물보호관리시스템 유기동물 조회 서비스)에 접속하고 조회를 할 수 있도록 **인증키**를 받아야 한다.
   
  *  http://apis.data.go.kr/1543061/abandonmentPublicSrvc/abandonmentPublic?bgnde=20211201&endde=20211231&pageNo=1&numOfRows=10&serviceKey=인증키(URL Encode)
   
   이 링크에 원하는 날짜, 페이지 번호, 페이지당 보여줄 개수를 수정하고 **인증키**를 넣으면 된다
    
* 키바나에 접속하고 기간은 2022년 8월 1일 ~ 2022년 8월 31일을 선정하기를 바란다. 다음 URL를 크릭하여 [Dashboard 유기동물](http://20.196.212.72:5601/app/dashboards#/view/760f8820-3454-11ed-bf24-f7c87035bdbc?_g=(filters:!(),refreshInterval:(pause:!t,value:0),time:(from:'2022-07-31T15:00:00.000Z',to:'2022-08-31T14:30:00.000Z')))  보여줄 것이다. <br>
 
 <h4 align="left"> 3. 데이터 를 분석  </h4>
   
 <h4 align="left"> 3.1: 응답 메시지 명세:  </h4>  
   동물보호관리시스템의 유기동물 정보 파일이다. 각 행의 정보는 다음과 같다.

   <p align="center">
 <img src="Images/abdm-table.PNG" style="width:500px;"/>
</p>
   
   품종 “ []” 로 구분 ([개] 믹스견) 한다.  이 프로젝트에 나중에 이 품종을 [“[개]”, “믹스견”] 같이 배열로 저장하기 위해 구분 한 것이다. 마잔가치로 공고번호 “충남-공주-2022-00001”는 [“충남”, “공주-2022-00001”]로 구분할 것이다.
 
<h4 align="left"> 3.2: Animal-center.csv:  </h4>  
   
  전국 동물보호센터 정보를 제공한다. 여러 행목이 있으나 Elastic Map Service 를 이용해서 표현하기 위한 “longitude”과 “latitude” 값을 이용하겠다. 그래서 필요한 정보만 수집하여 저장되었다. 다음 과 같다.
   
<p align="center">
  <img src="Images/abdm-center-table.PNG" style="width:400px;"/>
</p> 
   
 ### A. Method 1
   먼저 “animal-center.csv”파일을 색인하겠다. 카바나의 Data Visualizer 의 파일 업로드 기능을 이용해서 색인한 것이다.
위와 같이 키바나 기능을 이용하여 자동으로 “latitude” 과 “longitude”를 location (geo_point)으로 안다.
   
<p align="center">
  <img src="Images/kibana-animal-center.png" style="width:300px;"/>
</p>  
 <p align="center">     
  <em>그림 1: 전국 동물보호센터 정보 </em>
</p>
   
 ### B. Method 2
 1. Input and format data
 
 For each query from open API, we can get 1 page of 1000 rows data in one time. Our code download one by one page and append data into our MySQL database `Abandoment`
 
 ***Input***
 
 We use `sqlalchemy` library in Python to connect with our AWS server.
  
 ```python
db_connection_str = 'mysql+pymysql://admin:i4GSOM8GCjRfDyV@vteam6.cbr4uubmqr4e.ap-northeast-2.rds.amazonaws.com/Abandoment'
db_connection = create_engine(db_connection_str)
conn = db_connection.connect()
 ```
 
 ***Format***
 
 In the step of input, we format data before input into MySQL database. Use the format as in the instruction file (data.go.kr)
 ```python
 dtypesql = {'desertionNo':sqlalchemy.types.VARCHAR(15),
            'filename':sqlalchemy.types.VARCHAR(100), 
            'happenDt':sqlalchemy.Date(), #VARCHAR(8)
            'kindCd':sqlalchemy.types.VARCHAR(50),
            'colorCd':sqlalchemy.types.VARCHAR(30), 
            'age':sqlalchemy.types.VARCHAR(30), 
            'weight':sqlalchemy.types.VARCHAR(30),
            'noticeNo':sqlalchemy.types.VARCHAR(30),
            'noticeSdt':sqlalchemy.types.Date(), #VARCHAR(8)
            'noticeEdt':sqlalchemy.types.Date(), #VARCHAR(8)
            'popfile':sqlalchemy.types.VARCHAR(100),
            'processState':sqlalchemy.types.VARCHAR(10),
            'sexCd':sqlalchemy.types.VARCHAR(1),
            'neuterYn':sqlalchemy.types.VARCHAR(1),
            'specialMark':sqlalchemy.types.VARCHAR(200),
            'careNm':sqlalchemy.types.VARCHAR(50),
            'careTel':sqlalchemy.types.VARCHAR(14),
            'careAddr':sqlalchemy.types.VARCHAR(200),
            'orgNm':sqlalchemy.types.VARCHAR(50),
            'chargeNm':sqlalchemy.types.VARCHAR(20),
            'officetel':sqlalchemy.types.VARCHAR(14),
            'noticeComment':sqlalchemy.types.VARCHAR(200),
}
df.to_sql(name='aug', con=db_connection, if_exists='append', index=False,dtype=dtypesql)
 ```
*MySQL table:*

<img width="1080" alt="Screenshot 2022-09-15 034841" src="https://user-images.githubusercontent.com/79763166/190238822-fbd36e3e-4209-46da-a333-f95f0946847b.png" style="width:800px;"/>

 
 2. Push data from server to Kibanda by Logstash
 
***Input***

We already formated data so it's not necessary to format in Logstash

```logstash
input {
   jdbc {
      jdbc_driver_library => "/home/naviteam/.../mysql-connector-java-8.0.30.jar"
      jdbc_driver_class => "com.mysql.cj.jdbc.Driver"
      jdbc_connection_string => "jdbc:mysql://vteam6....:3306?Abandoment?characterEncoding=UTF-8&serverTimezone=UTC"
      jdbc_user => "ID"
      jdbc_password => "PASSWORD"
      statement =>"SELECT * from aug"
   }
}
```
***Filter***

filter를 이용하여 원하는 대로 데이터를 선정한다.
   * 첫째, `weight` field에서 체종만 필요하기 때문에 split를 이용하고 `weight_kg`이란 새로운 field를 생성하여 체종만 넣었다. 
   * 둘째, 위와 같이 품종별 잘 분석하기 위해 `kindcd` field([개] 믹스견)는 `kind` ([개]) 및 `subKind` (믹스견)으로 구분한다.
   * 셌째, 발견 도시를 알아보도록 `noticeno` field에서 `noticeCity` (인천, 서울,...)를 생성한다.
   * 넷째, 필요없는 field를 삭제하기 위해 "remove_field" 이용한다.

```logstash
filter {
mutate {
        split => ["[weight]", "("]
        add_field => { "weight_kg" => "%{[weight][0]}" }
        remove_field => ["weight"]
}
mutate {
        split => ["[kindcd]", " "]
        add_field => { "kind" => "%{[kindcd][0]}" }
        add_field => { "subKind" => "%{[kindcd][1]}" }
        remove_field => ["kindcd"]
}
mutate {
        split => ["[noticeno]", "-"]
        add_field => { "noticeCity" => "%{[noticeno][0]}" }
        }
mutate {
        join => { "[noticeno]" => "-" }
}
mutate {
        remove_field => ["@version", "@timestamp"]
}
}
```
***결과 확인***
   <p align="center">
 <img src="Images/logstash-3.PNG" style="width:500px;"/>
</p>
<p align = "center">
 <em>그림 2: logstash 결과 확인 </em>
</p>
   
<h4 align="left"> 3.4: 인덱스 매핑 </h4> 	
   
* 인덱스를 생성하여 원하는 형태로 매핑해야 한다. 키바나 콘솔에서 **“abandonment-info”** 인덱스를 만들면서 적용한다.
   <p align="center">
  <img src=" Images/abandonment-info-mapping-code.PNG " style="width:300px;"/>
</p>    
<p align = "center">
 <em>그림 3: mapping 코드 </em>
</p>

* "abandonment" 인덱스는 “abandonment-info” 인덱스 mapping으로 변경할 수 있기 위해 `_reindex` 를 이용한다.
 <p align="center">
  <img src=" Images/reindex.PNG " style="width:400px;"/>
</p> 
 <p align = "center">
 <em>그림 4: reindex 코드 및 결과 확인 </em>
</p>  

  * 그 후에 "abandonment" 인덱스를 삭제한면 된다.
   ```kibana
   DELETE abandonment
   ```
<h4 align="left">4. 키바나에서 데이터를 분석  </h4>  
   
자세한 내용은 다음 URL를 [Dashboard 유기동물](http://20.196.212.72:5601/app/dashboards#/view/760f8820-3454-11ed-bf24-f7c87035bdbc?_g=(filters:!(),refreshInterval:(pause:!t,value:0),time:(from:'2022-07-31T15:00:00.000Z',to:'2022-08-31T14:30:00.000Z'))) 접속하기를 바란다.
   
<h4 align="left">4.1. 사용자가 원하는 항목을 선택기능 만든다  </h4>  
 
 <p align="center">
  <img src=" Images/kibana-control.PNG" style="width:1000px;"/>
</p> 
   
 <p align="center">     
  <em>그림 5. Kibana-control 활용하기 </em>
</p>
    
<h4 align="left"> 4.2. 2022년 8월 1일 ~ 2022년 8월 31일:  </h4>
   접수건 및 일자별 접수건은 얼마인가? <br>
  조사 결과를 살펴보면 8월에 총 접수건이 10,621단위 있다. 가장 많이 유기동물을 접수한 날들이 1일 , 8일, 16일, 17일, 22일, 29일이었지만 22일에는 가장 높게 나타났다.
다음에는 상당적으로 유기동물을 접수한 날들이  2일, 9일, 19일, 25일, 29일이었는 데 29일에는 가장 접수한 것을 차지하였다. 마지막으로  21일, 28일에는 유기동물 접수일이 가장 낮은 것으로 조사되었다.
     
<p align="center">
 <img src="Images/총 접수건.PNG" style="width:250px;"/>
</p>

<p align="center">
 <img src="Images/일별 접수건.PNG" style="width:600px;"/>
</p>

 <p align="center">     
  <em>그림 6: 총 접수건 및 일별 접수건 </em>
</p>

<h4 align="left"> 4.3. 품종별 접수건 및 일별 품종별 접수건  </h4>
   품종별 및 일별 품종별 접수한 것에 대한 조사를 실시하였다. 조사 결과 개의 경우에는 접수건이 68.8%로 가장 높게 나타났으며 고양이의 경우에는 30.25%로 그 뒤를 이었다. 마지막으로 기타가 0.95%로 차지하였다.

<p align="center">
 <img src="Images/품종별 접수건.png" style="width:350px;"/>
</p>

<p align="center">
 <img src="Images/일별 품종별 접수건.png" style="width:500px;"/>
</p>

 <p align="center">     
  <em>그림 7: 일별 품종별 및 각 품종별 접수건 </em>
</p>

<h4 align="left"> 4.4. 주요접수 품종, 색상 및 특징  </h4>

<p align="center">
 <img src="Images/주요 품종 색상 특징.PNG" style="width:800px;"/>
</p>
 <p align="center">     
  <em>그림 8:  주요접수 품종, 색상 및 특징 </em>
</p>

   <h4 align="left"> 4.5. 성별과 중성화 관계 </h4>
   
   성별과 중성화 관계에 대한 설문조사를 실시하였다. 조사 경과 성별의 경우에는 M는 46.24%로 가장 높게 나타났으며 F는 44.9%로 그 뒤를 이었다. 마지막으로 Q는 8.86%로 조사되었다.
<p align="center">
 <img src="Images/성별 및 중성화.png" style="width:350px;"/>
</p>

 <p align="center">     
  <em>그림 9:  성별과 중성화 관계 </em>
</p>   
 <h4 align="left"> 4.6. 나이와 체중 관계 </h4>
<p align="center">
 <img src="Images/나이와 체종 관계.PNG" style="width:500px;"/>
</p>

 <p align="center">     
  <em>그림 10:  나이와 체중 관계 </em>
</p>
   
<h4 align="left"> 4.7. 보호소별 보호상태 및 품종별 </h4>
   
   히트맵을 통해 전국에 한국돌물구조권리협회, 제주 동물보호센터, 부산둥물보호센터에서 “보호중” 유기 둥물을 제일 많이 차지 하고 있다. 
 색상이 밝을수록 건수가 적다.
   
<p align="center">
 <img src="Images/보호소별 보호소 상태.PNG" style="width:550px;"/>
</p>
     
 <p align="center">     
  <em>그림 11: 보호소별 보호상태  </em>
</p>

<h4 align="left"> 4.8. 발견 도시별 접수 품종별 보호상태 히트맵 </h4>
   
<p align="center">  
 <img src="Images/발견도시별 품종별 보호상태.PNG" style="width:700px;"/>
</p>
   
 <p align="center">     
  <em>그림 12: 발견 도시별 접수 품종별 보호상태 히트맵 </em>
</p>
 
 <h4 align="left"> 4.9. 유기동물 </h4>
   
 <p align="center">
    
 <img src="Images/kibana-library.PNG" style="width:900px;"/>
</p>
   
 <p align="center">     
  <em>그림 13: 유기동물 library </em>
</p>
   
<h4 align="left"> 4.10. 전국동물보호센터 맵 </h4>
   
 <p align="center">   
 <img src="Images/전국동물보호센터 맵 및 히트맵.PNG" style="width:550px;"/>
</p>
   
 <p align="center">     
  <em>그림 14: 전국동물보호센터 맵 </em>
</p>
   히트냅을 보다시피 4.8와 같이 현재 "경기도"에서 접수건 및 "보호중" 유기동물이 제일 많고 마잔가지로 거기에 "동물보호센터"도 제일 많이 있다.  
 <h4 align="left"> 4.11. 전국동물보호센터 정보 </h4>
   
 <p align="center">   
 <img src="Images/전국동물보호센터 정보.PNG" style="width:750px;"/>
</p>
   
 <p align="center">     
  <em>그림 15: 전국동물보호센터 정보 </em>
</p>
   
<h3 align="left"> III. 유기동물 관리 웹사이트 개발 프로세스 </h3>
   
   9원 16일 전에  완성할 예정이다.
   
   
<h3 align="left"> IV. "CHATBOT" 성능 활용 </h3>
   
    9원 16일 전에  완성할 예정이다.
