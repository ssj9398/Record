# JS ����ϱ�
1. 3�ڸ� ���� �޸����
```
- toLocaleString() ex) https://github.com/ssj9398/FE-Study/blob/master/VanillaJs/localstring.html
```

2. alert���� Ȯ�� �� �̵�
```
alert('����',function(){
});
```

3. ��ũ���̵� �� ���� �ֱ�
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