# 201930216 배다슬
+ 팀명 : 프뉴비
+ 이름 : 배다슬(팀장: 디자인, 개발), 최기룡(팀원: 개발), 선정인(팀원: 디자인)
+ 졸업작품 소개 사이트 : https://das0166.github.io/frontnewbie/
+ 졸업작품 주제 : 일정 관리 웹 사이트

+ 작품 소개
    - 작품명 : 나의 하루를 책임질 '투데이'
    - 개발환경 : <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=HTML5&logoColor=white"> <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=CSS3&logoColor=white"> <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=React&logoColor=black"> <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=JavaScript&logoColor=white">
    - 작품 소개 : 오늘 해야할 일을 확인할 수 있는 투두 기능 및 캘린더 기능이 있는 사이트
    - 작품의 특징 : 캘린더 기능에 일정 추가까지 가능하여 제목, 시간, 장소 등을 작성할 수 있음

---
##  [ 2022년 10월 12일 ]
- 오류가 발생했던 것
    ![오류2](./%EC%98%A4%EB%A5%98/%EC%98%A4%EB%A5%982.png)
     - 발생한 이유 
        - useContext가 선언되지 않았기때문에 발생함
    - 해결 방법
        - import React, { useState } from "react";으로 작성 되었던 것을 import React, { useState, useContext } from "react";으로 수정했음

##  [ 2022년 10월 05일 ]
+ 오류가 발생했던 것
    ![오류1](./%EC%98%A4%EB%A5%98/%EC%98%A4%EB%A5%981.png)
    - 발생한 이유 
        - 구성 요소에서 사용하려는 경우 useState구성 요소가 대문자로 시작하고 함수 구성 요소인지 확인해야 함. 이를 어겼기때문에 오류가 발생한 것!
    - 해결 방법
        - 나의 경우 구성 요소 명을 'option'이라고 지정해두어 대문자로 시작해야한다는 점을 어겼음. 이를  해결 하기 위해선 'Option'으로 수정해야 함.
        
+ 어려웠던 것들
    - 메인 페이지 '옵션 더보기' 버튼 클릭 시 옵션 내용 보이게 하기 -> 옵션 내용을 새로운 js파일로 생성하여 만드는 것으로 해결 완료
    - 색상 레이어가 왼쪽에 보여질 때 투두 리스트와 메모지가 오른쪽으로 옮겨져야하는데 이를 수정해야할 방법을 찾아봐야함.

+ 추후 수정 필요한 것들
    - 색상 변경 레이어를 옵션 선택하는 곳에서 불러오기 때문에 위치와 크기가 이상함. 이를 margin을 이용하여 수정하였기 때문에 추후 해결 방안이 생긴하면 수정이 필요함

+ 11일까지 할 일
    - 색상 변경 레이어 팝업으로 시도해보기
    - 팝업이 안된다면 현 상황에서 수정해보기

##  [ 2022년 09월 28일 ]
+ 고려해야할 사항들
    - 모니터 크기를 1920px에 맞춰서 작업 후 반응형으로 하기
    - 메인 내용들을 position:absolute가 아닌 margin-top으로 정중앙 설정하기
    - ```main {height: calc(100vh - 70px);}``` (메인 높이는 header 높이를 제외한 나머지 부분이라는 것을 지정해주기 위해 작성하였음) 보류

+ 4일까지 할 일
    - 과제(포스터, ppt) 초기 시안 잡기
    - 메인 페이지 버튼 클릭시 왼쪽에 색상 변경하는 기능이 나올 수 있게 수정
    - 로그인 기능 추가 시도
    - todo 페이지에 있는 노트 크기 조정

##  [ 2022년 09월 21일 ]
+ 25일까지 할 일
    - 헤더 완성(완성)
    - 전반적인 React 학습
    - 메인 페이지 틀 잡기(완성)
    - 로그인 페이지 완성(기능 제외)(완성)

+ js 실행 방법 : npm start
+ 수정 사항이 있을 수도 있기 때문에 시작 전에 git pull
+ 이미지 적용 방법
    - src 폴더 안에 img 폴더 생성
    - img 폴더 안에 원하는 이미지 넣기
    - js 파일에서 import 및 이미지 불러오기
    ```js
    import logo from './image/today_logo.png';

    const Header = () => {
	return (
		<div className='header'>
            <img className='logo_img' src={logo} alt='logo'/>
		</div>
	);
    };
    export default Header;
    ```
+ App.js에서 header.js 불러오는 방법
    ```js
    import Header from './header.js';

   function App() {
    return(
        <div>
        <Header/>
        </div>
    )
    }

    export default App;
    ```
+ <></>는 ```<div></div>```와 같은 뜻
+ 코드를 작성하기 위해선 ```<div></div>```로 감싸야 한다!

##  [ 2022년 09월 14일 ]
+ 로고 완성  
    ![홈화면1](./img/%ED%88%AC%EB%8D%B0%EC%9D%B4_%EB%A1%9C%EA%B3%A0.png)

+ 팀원과 Git repository 연동
    - 팀원이 커밋 하면 Pull requests에 뜸, 이때 confirm을 해줘야 frontnewbie 폴더에 수정 사항이 연동됨

##  [ 2022년 09월 07일 ]
+ 팀규칙
    - 참여 : 팀 회의는 100% 참석하기, 결정된 참석 일정 일방적으로 불참하지 않기
    - 회의 : 일주일에 최소 1번 진행
    - 의견 : 자신의 의견은 자유롭게 얘기하기
    - 팀장 : 공평하게 진행될 수 있게 자유로운 분위기 조성
+ 작품기획(브레인스토밍)
    - 현재 상황
        - 일정 관리 및 Todo 웹 사이트를 만들고자 함
        - 프론트엔드로만 구성되어 있어 서버 및 DB 숙련도 부족
        - HTML, CSS에 특화된 팀원들로 구성되어 있기 때문에 기초적인 틀 개발은 문제 없음
        - React 및 JavaScript 숙련도 부족
        - 다른 사례들(캘린더, Toggl, Todoist)과 차별점을 두어야 함
    - 예상되는 결과물
        - 문제해결을 위한 실행 방법 : 공부를 병행하며 프로젝트 진행 예정, 벤치마킹을 진행하며 차별점을 구상할 예정 
        - 필요한 지식 및 기술 : HTML, CSS, React, JavaScript, DB
        - 예상되는 결과물 : Todo, 캘린더, 일정 관리
        - 회로도  
        ![회로도](./img/%ED%88%AC%EB%8D%B0%EC%9D%B4_%ED%9A%8C%EB%A1%9C%EB%8F%84.png)
+ 예상 결과물
    - 홈화면
    ![홈화면1](./img/%ED%88%AC%EB%8D%B0%EC%9D%B4_%ED%99%88%ED%99%94%EB%A9%B4.png)
    ![홈화면2](./img/%ED%88%AC%EB%8D%B0%EC%9D%B4_%ED%99%88%ED%99%94%EB%A9%B42.png)
    - 캘린더
    ![캘린더](./img/%ED%88%AC%EB%8D%B0%EC%9D%B4_%EC%BA%98%EB%A6%B0%EB%8D%94.png)
    - 로그인
    ![로그인](./img/%ED%88%AC%EB%8D%B0%EC%9D%B4_%EB%A1%9C%EA%B7%B8%EC%9D%B8.png)

+ 기능
    + 홈화면<br>
         &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**왼쪽 메모지**
        + 오늘 할 일이 보여짐(Todo)
        + today 왼쪽에 있는 edit 버튼을 누르면 메모지, 글 색상 등을 변경할 수 있으며 할 일을 추가할 수 있음
        + 화살표를 누르면 다음 날에 할 일을 확인할 수 있음<br> **오른쪽 메모지**
        + 포스트잇에는 오늘 날짜에 추가한 일정들이 나옴
    + 캘린더
        + 연도, 월, 주 단위로 캘린더를 볼 수 있음
        + 해당 날짜에 등록한 일정이 표시 됨
        + 생일이나 공휴일 등 주요 기념일 표시 됨
        + 오늘이 아닌 다른 날짜의 일정을 추가 할 수 있음
    + 로그인
        + 소셜 로그인도 가능



##  [ 2022년 08월 31일 ]
+ 팀명 : 프뉴비
+ 이름 : 배다슬(팀장: 디자인, 개발), 최기룡(팀원: 개발)
+ 졸업작품 소개 사이트 : https://das0166.github.io/frontnewbe/
+ 졸업작품 주제 : 일정 관리 웹 사이트

+ 작품 소개
    - 작품명 : 나의 하루를 책임질 '투데이'
    - 개발환경 : <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=HTML5&logoColor=white"> <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=CSS3&logoColor=white"> <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=React&logoColor=black"> <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=JavaScript&logoColor=white"> <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=MySQL&logoColor=white">
    - 작품 소개 : 오늘 해야할 일을 확인할 수 있는 투두 기능 및 캘린더 기능이 있는 사이트
    - 작품의 특징 : 캘린더 기능에 일정 추가까지 가능하여 제목, 시간, 장소 등을 작성할 수 있음
