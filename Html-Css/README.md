# HTML���
1. ������ �� �̹����� Ư���κ� url ��ũ �Ŵ¹�
- <img src="https://user-images.githubusercontent.com/48196352/116048685-61312e00-a6b0-11eb-9c1e-35041c6b779a.JPG" width="500">
- ��ǥ�� �׸��ǿ��� ���� �˼�����

2. �����Ϸ� â �ݱ�
- onclick�̺�Ʈ�� �̿��Ͽ� �Ʒ��� ���� function�� �߰����ش�.
- function setCookie(name, value, expiredays) {
			var todayDate = new Date();
			todayDate.setDate(todayDate.getDate() + expiredays);
			document.cookie = name + "=" + escape(value) + "; path=/; expires="
					+ todayDate.toGMTString() + ";";
		}

3. ajax�� ��� �� �� jsp���� ajax�� ��û�� �ϰ� ������ �ް� ���ƿ� response�� & �� ���ۼ�Ʈ�� ���� ��� ��û�� �޴��ʿ��� replac�� ġȯ�� ���־�� �Ѵ�.
- ���� �ڹ��� ���) VoName.getParamater().replace("&","&amp;");

# CSS ���
1. SelectBox ȭ��ǥ ��� �����ϰ� �ٸ��ɷ� �ٲٱ�
- select { -webkit-appearance: none; /* ����Ƽ�� ���� ���߱� */ - moz-appearance: none; 
 appearance: none; background: url(�̹��� ���) no-repeat 95% 50%; /* ȭ��ǥ ����� �̹��� */ }