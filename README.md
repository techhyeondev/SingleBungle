# ⭐️Portfolio - SingleBungle


<!-- contents -->
<details open="open">
  <summary>Contents</summary>
  <ol>
    <li>
      <a href="#개요">개요</a>
    </li>
    <li>
      <a href="#내용">내용</a>
    </li>
    <li><a href="#구현-기능">구현 기능</a>
      <ul>
        <li><a href="#공지사항-게시판">공지사항 게시판</a></li>
        <li><a href="#게시글-수정">만남의 광장 게시글 수정</a></li>
        <li><a href="#search">검색(카테고리)</a></li>
        <li><a href="#reply">댓글/답글 작성, 수정, 삭제, 신고</a></li>
        <li><a href="#참여신청">참여신청</a></li>
        <li><a href="#채팅">채팅</a></li>
      </ul>
    </li>
  </ol>
</details>

------------

# 📝개요

* 프로젝트 명 : SingleBungle

* 일정 : 2021년 01월 29일 ~ 2021년 03월 11일

* 개발 목적 : 1인 가구의 정보를 공유하고 소통할 수 있는 커뮤니티 사이트 제작

* 개발 환경
  - O/S : Windows 10
  - Server : Apache-tomcat-8.5.61
  - Java EE IDE : Eclipse ( version 2020-06 (4.16.0) )
  - Database : Oracle SQL Developer ( version 20.2.0 )
  - Programming Language : JAVA, HTML, CSS, JavaScript, JSP, SQL
  - Framework/flatform : Spring, mybatis, jQuery 3.5.1, Bootstrap v4.6.x
  - API : WebSocket, Kakao map, summernote
  - Version management : Git

------------

# 📝내용

* 팀원별 역할
  - 공통 : 기획, 요구 사항 정의, 와이어 프레임, DB 설계
  - 강수정 : 만남의 광장 게시판 CRUD, 채팅, 팀장
  - 강보령 : 싱글이의 영수증 게시판 CRUD, 쪽지
  - 김현혜 : 공지사항 게시판 CRUD, 고객센터 게시판 CRUD, 관리자, 기술고문
  - 신주희 : 회원가입, 로그인, 마이페이지
  - 이솔이 : 일상을 말해봐 게시판 CRUD, 먹보의 하루 게시판 CRUD
  - 이한솔 : 벙글 장터 게시판 CRUD

* 구현 기능
  - 공지사항 게시판 CRUD
  - 고객센터 게시판 CRUD
  - 관리자 기능 (회원 관리, 게시글 관리, 댓글 관리)


* DB 설계<br>
![singlebungle](https://user-images.githubusercontent.com/72387870/111110444-e7c9fa00-859f-11eb-926b-ac04e8e5d0ab.png)

------------

# 📝구현 기능

## 공지사항 게시판

 1. <h3>공지사항 조회</h3>

![공지사항 조회](https://user-images.githubusercontent.com/77372352/111657655-fd188000-884e-11eb-80ce-e4704c17f81c.gif)

  * 화면 설명 : 사이트 내 공지사항 게시판 페이지
   
  * 구현 기능 설명
    - 공지사항 게시판 글 목록 조회
    - 페이징을 통해 게시글 목록 넘기기
    - 공지사항 | 이벤트 탭을 통해 페이지 이동 가능
    - 관리자 회원만 글쓰기 가능
    - 게시글 상세 조회 (제목, 내용, 날짜, 조회수)
    - 관리자 회원만 수정/삭제 가능
    - 목록으로 이동


------------

2. <h3>공지사항 수정</h3>

   ![1_공지사항 게시글 수정](https://user-images.githubusercontent.com/77372352/111658733-f63e3d00-884f-11eb-8b62-4d10ae186660.gif)

 ![1_공지사항 게시글 수정](https://user-images.githubusercontent.com/77372352/111658733-f63e3d00-884f-11eb-8b62-4d10ae186660.gif)  * 구현 기능 설명   
   - 게시글 수정 시, DB에 등록된 게시글 제목, 내용 불러옴.
   - SummerNote Toolbar를 이용하여 글꼴 및 내용 수정.
   - 수정 버튼 클릭 시 수정한 게시글 상세조회로 이동하게 됩니다.<br>
    
------------

3. <h3>공지사항 게시글 삭제</h3>

  
   ![공지사항 게시글 삭제](https://user-images.githubusercontent.com/77372352/111660579-92b50f00-8851-11eb-8674-f7cc9be172e4.gif)
* 화면 설명 : 작성한 글을 삭제하고 싶은 경우 게시글을 삭제하는 페이지입니다.
 * 구현 기능 설명
    - 삭제 버튼 클릭 시 alert 창을 출력하여 한 번 더 확인할 수 있도록 했습니다.
    - alert 창에서 확인 클릭 시 글의 상태가 삭제로 바뀌며 게시글 목록으로 이동됩니다.

------------
## 이벤트 게시판


1. <h3>이벤트 조회</h3>

![enter image description here](https://user-images.githubusercontent.com/77372352/111664666-571c4400-8855-11eb-8978-275f50e2fb3c.gif)


  * 화면 설명 : 이벤트 게시판 목록 페이지
  
  * 구현 기능 설명
    - 이벤트 게시판 글 목록 조회
    - 사진이 등록된 게시글은 첫번째 사진으로 썸네일 등록
    - 썸네일이 없는 게시글은 기본 이미지로 대체
    - 클릭 시, 게시글 상세조회 페이지로 넘어감
    - 페이징 처리
    - 관리자 회원만 글쓰기 가능
    - 이미지가 등록된 게시글은 이미지도 함께 조회됨.


------------

<h3 id="reply">댓글/답글 작성, 수정, 삭제, 신고</h3>

  * 화면 설명 : 게시글에 댓글을 작성하는 화면입니다.
  ![댓글작성_수정](https://user-images.githubusercontent.com/72387870/111137572-4d2ee280-85c2-11eb-94ad-79956315899f.gif)
     
  * 구현 기능 설명
    - 댓글 작성 시 ajax를 통해 비동기적으로 등록한 댓글이 추가됩니다.
    - 댓글 수정 시 댓글 수정 내용을 입력할 수 있도록 기존 내용 영역이 textarea로 변경됩니다.
    - 수정 버튼 클릭 시 작성 시와 마찬가지로 ajax를 통해 댓글이 수정됩니다.
    - 답글 버튼 클릭 시 해당 댓글 영역 밑에 답글을 입력할 수 있는 textarea가 추가됩니다.
    - 답글 수정 버튼 클릭 시 댓글 수정과 마찬가지로 기존 내용 영역이 textarea로 변경됩니다.
    - 삭제 버튼 클릭 시 alert 창을 출력하여 한 번 더 확인할 수 있도록 했습니다.
    - alert 창에서 확인 클릭 시 답글 상태가 삭제로 바뀌며 ajax를 통해 댓글이 삭제됩니다.<br>
    ![답글작성_수정_삭제](https://user-images.githubusercontent.com/72387870/111137630-5e77ef00-85c2-11eb-8715-b946602df5b8.gif)
    - 타 회원의 부적절한 댓글은 신고를 클릭하여 신고할 수 있습니다.
    - 신고 제목, 신고 사유, 신고 내용을 입력하여 신고 버튼을 클릭하면 신고가 접수됩니다.
    ![6_댓글_신고](https://user-images.githubusercontent.com/72387870/111343823-260a0b00-86bf-11eb-957d-e77ea975b108.png)
  
------------  
  
## 참여신청

  * 화면 설명 : 원하는 친구 찾기 글에 참가신청 버튼을 클릭하여 참가할 수 있습니다.
  ![채팅하기_참여신청_채팅하기](https://user-images.githubusercontent.com/72387870/111138932-deeb1f80-85c3-11eb-9051-5520291b0855.gif)

  * 구현 기능 설명
    - 참가신청하지 않고 채팅하기 버튼을 클릭할 경우 알림 창을 출력할 수 있도록 구현했습니다.
    - 글 작성 시 지정한 모집인원수가 다 찬 경우에는 모집 신청 버튼이 모집 마감으로 변경되며<br> 
      더 이상 클릭할 수 없도록 구현했습니다.
    - 글 작성 시 지정한 모집 성별과 참여 신청 하는 회원의 성별이 다를 경우에는 참여 신청 할 수 없도록 구현했습니다.<br>
    ![참여신청_성별이 다를 경우](https://user-images.githubusercontent.com/72387870/111139196-2c678c80-85c4-11eb-98ec-04feea62c842.gif)
  
------------
  
## 채팅

  * 화면 설명 : 참여 신청한 회원들 간 실시간 채팅을 할 수 있는 화면입니다.<br>
  ![녹화_2021_03_15_21_48_54_714](https://user-images.githubusercontent.com/72387870/111155831-5165fa80-85d8-11eb-955f-d52d25326dad.gif)

  * 구현 기능 설명
    - WebSocket을 이용하여 실시간으로 채팅을 할 수 있습니다.
    - 자신이 보낸 채팅은 오른쪽에, 자신이 아닌 회원이 보낸 채팅은 왼쪽에 출력됩니다.
    - 채팅 내용은 저장이 되므로 이전의 채팅 내역을 볼 수 있습니다.<br>
    ![녹화_2021_03_15_22_05_51_72](https://user-images.githubusercontent.com/72387870/111157806-a86ccf00-85da-11eb-81d4-e536cffea636.gif)
    
------------
    
<p align="center">
감사합니다😄
</p>
