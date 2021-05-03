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
