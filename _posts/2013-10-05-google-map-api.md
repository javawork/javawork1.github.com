---
layout: post
title: "Google Map API"
description: ""
category: ""
tags: [nurserymap]
---

특정 지역의 어린이집 정보를 JSON형태로 가져옵니다.

``` javascript
$.getJSON(‘data/query’,{'area1':area1, 'area2':area2},function(data) {
...
}
```

아래와 같은 형태의 JSON데이터가 리턴됩니다.

``` json
[
{"own": "직장", "capacity": "35명", "title": "종로구청직장어린이집", "auth": "인증시설", "phone": "02-720-5852", "address": "서울특별시 종로구 삼봉로 43", "lat": 126.97912289999999, "lng": 37.572832839999997, "id": "11110000039"},{“own”: ...}
]
```

위도/경도 데이터로 marker를 생성합니다.

``` javascript
marker[index] = new google.maps.Marker({
	position: new google.maps.LatLng(lng, lat),
	map: map,
	title: data['title']
});
```

Marker를 클릭하면 보여줄 info_window를 만들고, 등록해 줍니다.

``` javascript
info_text = build_text_for_infowindow(data);
infowindow[index] = new google.maps.InfoWindow({
	content: info_text
});
google.maps.event.addListener(marker[index], 'click', function() {
	infowindow[this.index].open(map, marker[this.index]);
});
```
### Marker and Info window
![alt text]({{ site.url }}/assets/images/show_marker.png)

{% include JB/setup %}
