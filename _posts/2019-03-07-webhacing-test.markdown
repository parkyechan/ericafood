---
layout: post
title:  "비박스 환경을 활용한 웹 모의해킹 완벽 실습"
date:   2015-02-10 15:14:54
categories: Web-Hacking
---

### 비박스 환경을 활용한 웹 모의해킹 완벽 실습
* Chapter 4. SQL Injection
	* 4. 1 Get/Search
		* 새로 알게 된 점<br>
			sql injection 공격을 시행하는 데에 먼저 따옴표 '하나만 붙여서 테스트 한다는 사실에 대해서 알게 됨.<br>
			이 방식을 통해서 sql 질의문을 실행시켜 내가 원하는 값을 얻어올 수 있다는 사실을 배움. 그거까지 생각해본적은 없었던 것 같음.<br>
			특히 database 과목을 수강했지만 union select 구문에 대해서 다시 볼 수 있었고 union select 구문은 이전 질의와 출력 개수가 똑같아야 그 틀에 맞게 나온 다는 사실을 알게 됨.<br>
			그 틀 안에서 내용들을 출력하는데, 출력하는 내용을 찾을 때 table_name으로 시작해서 table 이름들을 쭉 훑어 보고 그 중에서 column을 선택하는 방법을 알게 됨.<br>
			특히 mysql 5.0이상의 버전에서는 information_schema.tables 와 같이 써야한다는 information_schema 에 대해서 배우게 됨.
		* 정답
			0' union select all 1, concat(id, login), password, email, 5, 6, 7 from users#
			
