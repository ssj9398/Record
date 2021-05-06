# HTML기록
1. 통으로 된 이미지에 특정부분 url 링크 거는법
- <img src="https://user-images.githubusercontent.com/48196352/116048685-61312e00-a6b0-11eb-9c1e-35041c6b779a.JPG" width="500">
- 좌표는 그림판열면 쉽게 알수있음

2. 오늘하루 창 닫기
- onclick이벤트를 이용하여 아래와 같이 function을 추가해준다.
- function setCookie(name, value, expiredays) {
			var todayDate = new Date();
			todayDate.setDate(todayDate.getDate() + expiredays);
			document.cookie = name + "=" + escape(value) + "; path=/; expires="
					+ todayDate.toGMTString() + ";";
		}

3. ajax를 사용 할 때 jsp에서 ajax로 요청을 하고 응답을 받고 날아온 response에 & 즉 엠퍼센트가 있을 경우 요청을 받는쪽에서 replac로 치환을 해주어야 한다.
- 예시 자바일 경우) VoName.getParamater().replace("&","&amp;");

# CSS 기록
1. SelectBox 화살표 모양 제거하고 다른걸로 바꾸기
- select { -webkit-appearance: none; /* 네이티브 외형 감추기 */ - moz-appearance: none; 
 appearance: none; background: url(이미지 경로) no-repeat 95% 50%; /* 화살표 모양의 이미지 */ }