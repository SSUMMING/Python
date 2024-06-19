# Python 새로 알게된 문법/코드 정리 🗒️

### 🟡 문자가 대문자인지 소문자인지 판별하는 Method
- str.isupper() 문자열이 대문자인지 판별 -> bool 형태의 결과 return
- str.islower() 문자열이 소문자인지 판별 > bool 형태의 결과 return  

---

### 🟡 대문자는 소문자로, 소문자는 대문자로 변환해주는 Method
- str.swapcase()

---

### 🟡 sep
- print문의 매개변수 sep, separation의 약자로 print문에 입력된 여러 항목을 "어떻게 분리할 것인가" 를 나타낸다.

예시
- print('안', '녕', '하', '세', '요') 🔜 안 녕 하 세 요 (기본적으로 띄어쓰기가 되어서 return)
- print('안', '녕', '하', '세', '요', sep='') 🔜 안녕하세요 (sep을 이용해 공백을 없애줌)
- print(1, 2, 3, sep=',') 🔜 1,2,3

---

### 🟡 replace
- replace(기존문자열, 바꿀문자열) 에서 replace는 문자열의 특정 위치를 지정하지 않고, 문자열 전체에서 일치하는 부분 문자열을 교체한다.

- 내가 쓴 오답  
  def solution(my_string, overwrite_string, s):  
       answer = my_string.replace(my_string[s:s+len(overwrite_string)],overwrite_string)   

- 오답 노트  
  string = 'abcabc' 이고 나는 3번째 자리부터 끝까지 문자열 'xyz'로 교체하고싶다.
  그러나 string.replace(string[3:],'xyz')를 쓰면 🔜 'xyzxyz'가 나온다 왜일까??

  replace는 문자열의 특정 위치를 지정하는 것이 아니고, 내가 슬라이싱한 부분의 문자열'abc'자체를 xyz로 바꿔주는 것이다!
  즉, abc를 xyz로 바꿔라 라는 코드를 짠것이다.

- 해결방법  
  replace가 아니고 문자열을 슬라이싱해서 +  문자열을 연결시킨다
  
  def solution(my_string, overwrite_string, s):  
     before = my_string[:s]  
     after = my_string[s+len(overwrite_string):]  
     answer = before + overwrite_string + after  
     return answer

---

### 🟡 Boolean
- Boolean 사용법 IN 조건문
- if (조건문):   
         수행문        => 조건문이 True일 때, 수행문(조건문 내부코드)를 실행하라!

- 예시   
  is_raining = True   


  if is_raining:   
           print("Take an umbrella!")
  
  else:   
           print("No need for an umbrella today.")

