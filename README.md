# Python 새로 알게된 문법/코드 정리 🗒️

### 🟡 문자가 대문자인지 소문자인지 판별하는 Method
- str.isupper() 문자열이 대문자인지 판별 -> bool 형태의 결과 return
- str.islower() 문자열이 소문자인지 판별 > bool 형태의 결과 return


### 🟡 대문자는 소문자로, 소문자는 대문자로 변환해주는 Method
- str.swapcase()

### 🟡 sep
- print문의 매개변수 sep, separation의 약자로 print문에 입력된 여러 항목을 "어떻게 분리할 것인가" 를 나타낸다.

예시
- print('안', '녕', '하', '세', '요') 🔜 안 녕 하 세 요 (기본적으로 띄어쓰기가 되어서 return)
- print('안', '녕', '하', '세', '요', sep='') 🔜 안녕하세요 (sep을 이용해 공백을 없애줌)
- print(1, 2, 3, sep=',') 🔜 1,2,3

