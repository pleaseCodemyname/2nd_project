# 🍳 코로나 이후 일본여행에 대한 트랜드 분석 🔍 
<br/>

##  ✔ 시작가이드
### 🛬 For building and running the application you need :
> - Python 3.10.12
> - mongodb 4.4.25
> - Linux Ubuntu 22.04

### 🛬 Installation
```
# git clone https://github.com/pleaseCodemyname/2nd_project.git
```
### 🛬 How to Start
```
# pip install --upgrade pip
# pip install fastapi uvicorn google-api-python-client pymongo matplotlib pandas numpy
# uvicorn main:app --host 0.0.0.0 --port 3000 --reload
```
<br/>

### ✔ 기술스택
|Category|Language|
|:--:|:--|
|OS|![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black) ![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)|
|Frontend|![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white) ![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white) ![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E) |
|Backend|![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi) |
|Database|![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white)|

<br/>

### ✔ 프로젝트 개요
> - 팀명 : 오디가조
> - 인원 : 3인 [ 강지연, 윤상현, 차아린 ]
> - 역할 : YoutubeAPI를 통해 데이터를 추출하고 가공하여 데이터를 시각화 하는 작업
> - 기간 : 2023.05 ~ 2023.06
> - 문서 : Architecture, API 설계서, 실행화면
<br/>

### ✔ 프로젝트를 선정하게 된 계기
> - 코로나가 시작된 이후 다양한 산업이 막대한 피해를 받았는데, 그 중에서도, 여행업계가 많은 타격을 입었다고 생각합니다. 그래서 코로나 이후로 얼마나 여행 트랜드가 변했는지에 대해 알아보고 싶었습니다.
> - 그 중에서도 일본 여행을 가고자 하는 여행객들에게 어떤 여행지로 많이 여행을 가는지를 분석해서 보여주면 선택에 영향을 미칠 수 있을 것이라 생각했고, 관광업체에서도 이러한 데이터를 바탕으로 비교분석하여 향후를 특정 여행코스에 대해 더 준비를 할 수 있다고 생각하여 개발하게 되었습니다.
<br/>

### ✔ 프로젝트 요약
> - YoutubeAPI를 활용하여 일본 여행에 대한 데이터 크롤링(아이디, 제목, 게시날짜, 조회수, Tags)
> - 2018, 2020, 2022, 2023 크롤링한 데이터를 기반으로 "됴쿄", "오사카", "후쿠오카"가 
5개씩 월별로 데이터 추출
> - 추출한 데이터를 바탕으로 연도별 월별 그래프 생성 및 전체 그래프 생성 및 비교분석 
<br/>

### ✔ 프로젝트 목적
> - 코로나 이후로 일본 여행의 인기여행지의 수요가 얼마나 증가 or 감소했는지 파악하기 위함
<br/>

### ✔ 아키텍처
![그림](https://github.com/pleaseCodemyname/2nd_project/blob/main/images/architecture.png) 
> - PYTHON FastAPI를 활용하여 기능구현 ( YoutubeAPI를 활용한 크롤링, DB연결, 데이터 가공, 웹 프로그래밍 )
<br/>

### ✔ API 설계서
![API설계서1](https://github.com/pleaseCodemyname/2nd_project/blob/main/images/2nd_Project_API(1).png)
![API설계서2](https://github.com/pleaseCodemyname/2nd_project/blob/main/images/2nd_Project_API(2).png)
![API설계서3](https://github.com/pleaseCodemyname/2nd_project/blob/main/images/2nd_Project_API(3).png)
![API설계서4](https://github.com/pleaseCodemyname/2nd_project/blob/main/images/2nd_Project_API(4).png)
![API설계서5](https://github.com/pleaseCodemyname/2nd_project/blob/main/images/2nd_Project_API(5).png)
###  ✔ 개발 과정

> - 크롤링한 데이터의 특정도시의 언급 횟수를 Count하거나 그래프를 만들어 시각화를 하려면 From Json To List로 전환하는 가공하는 작업이 필요했습니다.
> - YoutubeAPI를 통해 가져온 데이터를  MongoDB에 저장 했고, JSON -> List 데이터 가공 후 도시별 언급 횟수 및 그래프 생성까지 진행했습니다.
<br/>

###  ✔ 실행 화면
| 메인 페이지  |  실행 페이지(1)   |
| :-------------------------------------------: | :------------: |
|  <img width="329" src="https://github.com/pleaseCodemyname/2nd_project/blob/main/2nd_proj(1).png"/> | <img width="329" src="https://github.com/pleaseCodemyname/2nd_project/blob/main/images/2nd_proj(2).png"/>|

<br/>

###  ✔ 개선 방향
> - 일본 인기 여행지 뿐만 아니라 각국 여행지를 포함하여 데이터를 분석하고 시각화 할 수 있으면 더 좋은 서비스가 될 것이라 생각합니다.