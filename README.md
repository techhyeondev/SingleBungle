﻿# ⭐️Portfolio - SingleBungle


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
        <li><a href="#notice">공지사항 게시판</a></li>
        <li><a href="#event">이벤트 게시판</a></li>
        <li><a href="#faq">FAQ 게시판</a></li>
        <li><a href="#inquiry">1 : 1 문의 게시판</a></li>
        <li><a href="#member">관리자 - 회원 관리</a></li>
        <li><a href="#board">관리자 - 게시글 관리</a></li>
        <li><a href="#reply">관리자 - 댓글 관리</a></li>
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

 1. <h3 id="notice">공지사항 조회</h3>

![공지사항 조회](https://user-images.githubusercontent.com/77372352/111657655-fd188000-884e-11eb-80ce-e4704c17f81c.gif)

  **사이트 내 공지사항 게시판 페이지**
   
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

**공지사항 게시글 수정 페이지**
  * 구현 기능 설명   
	   - 게시글 수정 시, DB에 등록된 게시글 제목, 내용 불러옴.
	   - SummerNote Toolbar를 이용하여 글꼴 및 내용 수정.
	   - 수정 버튼 클릭 시 수정한 게시글 상세조회로 이동하게 됩니다.<br>
    
------------

3. <h3>공지사항 게시글 삭제</h3>

  
   ![공지사항 게시글 삭제](https://user-images.githubusercontent.com/77372352/111660579-92b50f00-8851-11eb-8674-f7cc9be172e4.gif)

**작성한 게시글 삭제**

 * 구현 기능 설명
    - 삭제 버튼 클릭 시 alert 창을 출력하여 한 번 더 확인할 수 있도록 했습니다.
    - alert 창에서 확인 클릭 시 글의 상태가 삭제로 바뀌며 게시글 목록으로 이동됩니다.

------------
## 이벤트 게시판


1. <h3 id="event">이벤트 조회</h3>

![enter image description here](https://user-images.githubusercontent.com/77372352/111664666-571c4400-8855-11eb-8978-275f50e2fb3c.gif)


  **이벤트 게시판 목록 페이지**
  
  * 구현 기능 설명
    - 이벤트 게시판 글 목록 조회
    - 사진이 등록된 게시글은 첫번째 사진으로 썸네일 등록
    - 썸네일이 없는 게시글은 기본 이미지로 대체
    - 클릭 시, 게시글 상세조회 페이지로 넘어감
    - 페이징 처리
    - 관리자 회원만 글쓰기 가능
    - 이미지가 등록된 게시글은 이미지도 함께 조회됨.


------------

2. <h3>이벤트 게시판 수정</h3>

![이벤트 게시판 수정](https://user-images.githubusercontent.com/77372352/111767342-f5f28000-88e9-11eb-8c15-4cbdefed145a.gif)

  **이벤트 게시글 수정**
 
  * 구현 기능 설명
    -  SummerNote를 활용한 게시글 작성 구현.
    -  게시글 수정 시, DB에 등록된 게시글 제목, 내용 불러옴.
    - SummerNote Toolbar를 이용하여 글꼴 및 내용 수정.
    - 이미지가 등록된 게시글의 경우, 이미지도 함께 수정 가능.
    - 등록 클릭 시, 해당 내용으로 DB에 등록.


------------  
  
3. <h3>이벤트 게시글 삭제</h3>

![enter image description here](https://user-images.githubusercontent.com/77372352/111767979-af515580-88ea-11eb-86aa-3dce5710db00.gif)

**작성한 글을 삭제하고 싶은 경우 게시글을 삭제**

 * 구현 기능 설명
    - 삭제 버튼 클릭 시 alert 창을 출력하여 한 번 더 확인할 수 있도록 했습니다.
    - alert 창에서 확인 클릭 시 글의 상태가 삭제로 바뀌며 게시글 목록으로 이동.<br>
    
------------
## FAQ 게시판

1. <h3 id="faq">FAQ 게시판 조회</h3>
![enter image description here](https://user-images.githubusercontent.com/77372352/111773331-63ee7580-88f1-11eb-8757-1bea25053acf.gif)

**FAQ 게시판 조회**

 * 구현 기능 설명
    - 회원들이 자주 묻는 FAQ를 한눈에 보기 편하게 조회.
    - 질문 클릭 시, 해당 질문에 대한 답변이 아코디언 형식으로 보여짐.
    - 카테고리 클릭 시, 해당 카테고리에 대한 FAQ만 조회
    - FAQ | 1:1 문의 클릭 시 해당 페이지로 넘어감.
    - 관리자만 FAQ 작성 가능

------------

2. <h3>FAQ 작성</h3>
![FAQ 작성](https://user-images.githubusercontent.com/77372352/111773211-36093100-88f1-11eb-85ba-f33debc0246f.gif)

**FAQ 작성**

 * 구현 기능 설명
    - SummerNote를 활용한 게시글 작성 구현.
    - SummerNote Toolbar를 이용하여 글꼴 및 내용 수정.
    - 카테고리를 선택할 수 있게함.
    - 등록 클릭 시, 해당 내용으로 DB에 등록.

------------
## 1 : 1 문의 게시판

1. <h3 id="inquiry">1:1문의 게시판 조회</h3>
![enter image description here](https://user-images.githubusercontent.com/77372352/111774654-1b37bc00-88f3-11eb-9e1f-d31f9e05a5e3.png)

**1:1문의 게시판 조회 - 일반 회원**

 * 구현 기능 설명
    - 회원 개인마다 자신이 남긴 1:1 문의만 조회 가능.
    - 관리자의 답변이 달린 경우 답변 여부의 이미지가 바뀜
    - 글 클릭 시, 해당 문의 사항 상세 조회로 넘어감.



![1:1문의 게시판 조회](https://user-images.githubusercontent.com/77372352/111774381-bb411580-88f2-11eb-83e8-d2116d0a6df3.gif)

**1:1문의 게시판 조회 - 관리자**

 * 구현 기능 설명
    - 모든 회원이 남긴 1:1 문의 조회 가능.
    - 관리자의 답변이 달린 경우 답변 여부의 이미지가 바뀜
    - 글 클릭 시, 해당 문의 사항 상세 조회로 넘어감.
    
------------
2. <h3>1:1 문의 게시글 작성 - 일반 회원</h3>
![enter image description here](https://user-images.githubusercontent.com/77372352/111776138-fcd2c000-88f4-11eb-988a-4f345e7d0169.gif)

**1:1문의 게시글 작성 - 일반 회원**

 * 구현 기능 설명
    - 회원 별로 1:1 문의 게시글 작성 가능
    - 문의 유형 카테고리 선택 가능
    
-------------

3. <h3>1:1 문의 게시글 답변 작성 - 관리자</h3>
![enter image description here](https://user-images.githubusercontent.com/77372352/111776552-81254300-88f5-11eb-8597-70db3d9fec0f.gif)

**1:1문의 답변 작성 - 관리자**

 * 구현 기능 설명
    - 관리자만 댓글로 답변을 남길 수가 있음.
    - 답변을 남기고 나면 수정/삭제 불가능
    - 답변이 달리면 답변 여부 아이콘 바뀜

------------
  

## 관리자 - 회원 관리

1. <h3 id="member">전체 회원 관리</h3>

![전체회원관리](https://user-images.githubusercontent.com/77372352/111768907-e3794600-88eb-11eb-81ef-4d6c58332430.gif)

  **활동 중, 탈퇴 중인 회원 모두를 조회하고 관리**
  
  * 구현 기능 설명
    - 모든 회원 조회 가능
    - 등급 별로 회원 조회 가능함.
    - 선택한 회원만 강퇴 시키거나, 강퇴 상태에서 복구 시킬 수 있음
    - 페이징 처리

-------------

2. <h3>회원 등급 관리</h3>
    ![회원 등급 관리](https://user-images.githubusercontent.com/77372352/111769506-a6fa1a00-88ec-11eb-8990-9ebb02189645.gif)


**관리자 회원의 등업 관리**
  
 * 구현 기능 설명
	  - 특정 조건을 채운 회원의 등급 조회 가능
    - 등급별로 회원 조회 가능함.
    - 선택한 회원만 레벨업을 승인할 수 있음
    - 페이징 처리

------------

## 관리자 - 게시글 관리

1. <h3 id="board">삭제된 게시글 관리</h3>

![삭제된 게시글 관리](https://user-images.githubusercontent.com/77372352/111770521-dcebce00-88ed-11eb-8a9f-6ad693f2bf8c.gif)

**삭제된 게시글 관리**

* 구현 기능 설명
	- 삭제처리된 게시글을 전체 조회 가능
	- 게시판 별로 조회 가능함.
	- 선택한 게시글만 복구처리 가능
	- 클릭 시 어떤 게시글인지 조회 가능
	 - 페이징 처리
 
------------

2. <h3>신고 게시글 관리</h3>

![신고 게시글 관리](https://user-images.githubusercontent.com/77372352/111771400-fe00ee80-88ee-11eb-9268-9df3649dee6f.gif)

**신고된 게시글 관리**

* 구현 기능 설명
	- 신고처리된 게시글을 전체 조회 가능
	- 신고 카테고리 별로 조회 가능함.
	- 선택한 게시글만 신고 취소 / 게시글 삭제 처리
	- 클릭 시 어떤 게시글인지 조회 가능
	- 페이징 처리

------------

## 관리자 - 댓글 관리

1. <h3 id="reply">삭제된 댓글 관리</h3>
![삭제된 댓글 관리](https://user-images.githubusercontent.com/77372352/111772238-fee65000-88ef-11eb-84d2-b85ecb874c84.gif)

**삭제된 댓글 관리**

* 구현 기능 설명
	- 삭제처리된 댓글을 전체 조회 가능
	- 게시판 별로 조회 가능함.
	- 선택한 댓글만 복구 처리 가능
	- 페이징 처리
------------
2. <h3>신고 댓글 관리</h3>
![신고 댓글 관리](https://user-images.githubusercontent.com/77372352/111772615-66040480-88f0-11eb-974e-4632ca4a4d90.gif)

**신고된 댓글 관리**

* 구현 기능 설명
	- 신고처리된 댓글을 전체 조회 가능
	- 신고 카테고리 별로 조회 가능함.
	- 선택한 댓글만 신고 취소 / 게시글 삭제 처리
	- 페이징 처리

------------
    
<p align="center">
지금까지 읽어주셔서 감사합니다:)<br><br>
추가적인 포트폴리오가 궁금하시다면 <br>
[포트폴리오 링크](https://techhyeondev.github.io/) 를 클릭해주세요~
</p>
