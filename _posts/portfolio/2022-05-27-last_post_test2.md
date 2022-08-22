---
layout: post
title: ROTUTEE
tags: 온라인교육플랫폼
description: >
  Final project
sitemap: false
hide_last_modified: false
categories:
  - portfolio
---

## ✏️개발자를 위한 강의 사이트 'ROTUTEE'✏️

* toc
{:toc .large-only}
toc_sticky: true

### 프로젝트 진행 기간

### 개발 인원

> 4인 <br/>
> 역할: DBA & Tester

### 업무분석 및 요건정의 : 2022-03-17 ~ 2022-04-01

### 개발환경

> **Java11**, **Oracle**, **HTML/CSS**, **JavaScript**, **Spring Boot 2.6.6**, **Thymeleaf**, **JPA**

### 사용 Tool

> **Intellij**, **DBeaver**, **Visual Studio Code**

### 형상관리 Tool

> **GitLab**, **SouceTree**

### 개발 Process

> **Waterfall 방식** 

* * *

## 1. 기획

### 1-1. 프로젝트 소개

ЯOTUTEE는 **Quiz, ToDo, 질의응답 게시판** 등을 포함한 **LMS** 기능을 추가해
기존의 단방향적인 강의 프로그램에서 벗어난 **자기주도적** 학습을 돕는 **IT 개발 전문 온라인 교육 플랫폼** 입니다.

<details>
<summary>세부 일자</summary>
<div markdown="1">
업무분석 : 2022-03-17 ~ 2022-03-19<br>
요구사항분석 : 2022-03-19 ~ 2022-03-20<br>
Use Case 다이어그램 : 2022-03-19 ~ 2022-03-20<br>
업무목록 : 2022-03-20 ~ 2022-03-22<br>
전체업무흐름도 : 2022-03-20 ~ 2022-03-21<br>
단위업무정의 : 2022-03-21 ~ 2022-03-23<br>
프로토타이핑 : 2022-03-24 ~ 2022-04-01<br>
</div>
</details>

[진행 기간 상세 Notion Link](https://broken-zebra-b49.notion.site/ROTUTEE-WBS-bc3dcd0f8bf74ca8a5fdf92c88df716c "rotutee wbs")

### 1-2. 기획 의도

> **비대면 교육의 증가**
>
> 2020년 covid19로 의해 비대면 강의 트랜드가 급격히 확산되었습니다. 비대면 강의의 증가를 토대로 여러 온라인 교육 플랫폼에 대하여 조사해본 결과, 대다수의 온라인 교육 플랫폼이 단방향적인 강의 방식으로 강의를 진행하고 있다는 것을 알았습니다. 이러한 기존 온라인 강의의 방식 개선을 위해 **튜터 제도**, **LMS(퀴즈, ToDo, 질의 응답)**, 강의 시청을 유도하기 위한 **룰렛 포인트 시스템**을 도입하여 재미와 교육 2가지를 합친 플랫폼인 **ROTUTEE**를 기획하게 되었습니다.

> **IT 교육의 중요성**
>
> 4차 산업혁명으로 IT 산업의 가속화와 더불어 팬데믹에 따른 디지털 전환의 가속화로 IT 역량의 중요성이 더욱 증가하고 있습니다. 현재의 패러다임에 맞춰 **IT 중심 교육 플랫폼**을 기획하였습니다.

자세한 사항은 Notion을 참고해 주시길 바랍니다.

🚩상세 Notion 링크 : [프로젝트 소개](https://broken-zebra-b49.notion.site/22a7a5ee8bec4da784ec2af65547d981 "project intro")

### 1-3. 시장조사

![시장조사1](/assets/img/portfolio/rotutee/market-research1.png){: width="800"}

[원본](/assets/img/portfolio/rotutee/market-research1.png)

![시장조사2](/assets/img/portfolio/rotutee/market-research2.png){: width="800"}

[원본](/assets/img/portfolio/rotutee/market-research2.png)

![시장조사3](/assets/img/portfolio/rotutee/market-research3.png){: width="800"}

[원본](/assets/img/portfolio/rotutee/market-research3.png)

### 1-4. 유사 프로그램 분석

> 개발자들의 공부를 돕는 온라인 강의 사이트 위주로 조사를 진행하였습니다.
> 1. 코드잇 : 개발 입문자가 사용하기 좋은 사이트, 직접 코드를 작성 할 수 있어 교육에 도움이 됩니다.
> 
> 2. 인프런 : 프로그래밍 외에도 다양한 분야의 강의가 존재하지만 프로그래밍 분야의 강의가 유명, 강의의 기한이 무제한인 점과 비교적 저렴한 가격이 장점입니다. 단점으로는 단방향 교육 형식으로 본인의 의지가 있지 않고서는 원활한 진행이 어렵고 지식공유자의 명확한 선정기준이 없다는 것입니다.
> 
> 3. 패스트 캠퍼스 : 무제한 수강이 가능하다는 것이 장점이나 실무자의 강의 진행으로 강의성 퀄리티를 기대하기는 어렵습니다.

![유사프로그램 분석](/assets/img/portfolio/rotutee/analyze-program.PNG)

🚩상세 Notion 링크 : [유사프로그램 분석](https://broken-zebra-b49.notion.site/7e2d424b58c7496382461a6b76546939)

### 1-5. 주요 기능

> 주요기능 도출은 프로젝트 기획을 바탕으로 필수 기능, 필수 기능과 상호작용되는 서브 기능 순으로 도출 하였습니다. 그 다음 서비스의 이용자 권한을 기준으로 기능을 분류하였습니다.
<br/>

> 서비스의 중심인 강의를 기준으로 강의 시청, 강의 영상 업로드 등을 서비스의 목적에 맞게 도출하였습니다.

![기능 도출 예시](/assets/img/portfolio/rotutee/primary-function.jpg){: width="800"}

🚩상세 Notion 링크 : [주요 기능](https://broken-zebra-b49.notion.site/6f9e50f77e1746258f85ba332996a42c)

* * *

## 2. 업무 분석 및 요건 정의

### 2-1. 요구사항명세

![요구사항명세](/assets/img/portfolio/rotutee/require.PNG){: width="800"}

🚩상세 Notion 링크 : [주요 기능](https://broken-zebra-b49.notion.site/551a4aea43964464b213d5738056fed5)

### 2-2. 전체업무흐름도

![전체업무흐름도](/assets/img/portfolio/rotutee/entire-task-diagram.PNG){: width="800"}

### 2-3. 단위업무흐름도

![전체업무흐름도](/assets/img/portfolio/rotutee/unit-task-sample.PNG){: width="800"}

🚩상세 Notion 링크 : [주요 기능](https://broken-zebra-b49.notion.site/5396b0d2682e46fe881d3149e736a47f)

* * *

## 3. 설계

### 3-1. 논리 데이터 베이스 모델(ERD)

![전체업무흐름도](/assets/img/portfolio/rotutee/DB_ERD_Final.png){: width="800"}

### 3-2. ERD 설계 시 고려한 점

-  PK 설정
- 중복 데이터 제거
- 관계 설정 후 재검토
- 필드명 통일




