# JS 기록하기
1. 3자리 마다 콤마찍기
```
- toLocaleString() ex) https://github.com/ssj9398/FE-Study/blob/master/VanillaJs/localstring.html
```

2. alert띄우고 확인 후 이동
```
alert('내용',function(){
});
```

3. 스크롤이동 시 색상 넣기
```
window.addEventListener("scroll",function(){
	var height = window.pageYOffset;
	var gnbWrap = document.querySelector(".gnbWrap");

	gnbWrap.style.backgroundColor="#dedede";
	if(height==0){
		gnbWrap.style.backgroundColor="white";
	}
});

```