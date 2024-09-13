# Google Colab & Github 연동 방법


### 1. Google Drive 에 폴더 생성
<img width="1174" alt="스크린샷 2024-09-13 17 32 06" src="https://github.com/user-attachments/assets/80ebe906-75a1-46a2-9665-85bf87744b4f">

### 2. Github 연동하기

#### 1. 구글 드라이브 연동

~~~python
import os
from google.colab import drive
drive.mount('/content/drive/')
~~~

> Mounted at /content/drive/ 

#### 2. 생성 폴더로 이동

~~~python
# 위에서 생성한 폴더 위치 ex) /content/drive/MyDrive/Daou_FiveGuys
cd /content/drive/MyDrive/
~~~

> /content/drive/MyDrive/Daou_FiveGuys

#### 3. Git Clone

~~~python
!git clone https://[깃허브 아이디]:[토큰]@github.com/Daou-FiveGuys/colab.git
~~~

> Cloning into 'colab'...
	remote: Enumerating objects: 4, done.
	remote: Counting objects: 100% (4/4), done.
	remote: Compressing objects: 100% (3/3), done.
	remote: Total 4 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
	Receiving objects: 100% (4/4), done.

#### 4. 권한 부여
~~~python
!git config --global user.email '깃허브 이메일'
!git config --global user.name '깃허브 아이디'
~~~

### 🎉 연동 완료 🎉 
