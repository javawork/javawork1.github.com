---
layout: post
title: "NurseryMap Intro"
description: ""
category: "nurserymap"
tags: [nurserymap]
---

`Google Map API`와 `Google App Engine`을 이용해서 지도상에서 어린이집을 표시해주는 서비스를 만들었습니다.

[우리동네 어린이집](http://nurserymap.appspot.com/)

같은 서비스를 `Daum Map`과 `PHP`를 사용해서 만든적이 있었는데, 데이터 수집이 너무 어려워서 서울/경기 지역만 수집하고 중단했었습니다.

[이전 서비스](http://placardmart.com/)

이번에는 `Google App Engine`의 `cron job` 기능으로 전국 데이터를 수집할 수 있었고, 새로운 기능도 추가할 수 있었습니다. 

### 서비스 구분 

이 서비스는 크게 데이터를 수집하는 부분과 수집된 데이터를 지도상에 표시해주는 부분으로 나눌 수 있습니다.

### 데이터 수집

### 지도상에서 보여주기

{% include JB/setup %}
