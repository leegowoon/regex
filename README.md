# 🌼정규표현식
# /regex/ : Regular expression의 약자

# 언제 사용하는가?
- 텍스트에서 우리가 원하는 특정한 패턴을 찾을 때 (전화번호형태의 패턴, 웹사이트주소형태의 패턴, 이메일형식의 패턴을 찾을 때)
- 사용자가 입력한 텍스트가 이메일이나 패스워드와 같이 특정한 패턴에 부합하는지 유효성검사를 할 때도 사용할 수 있다.
- 정규식은 문자를 검사하고자할 때 사용하는 식이다.

# 정규식은 /(슬래시)로 시작하여 "나는 정규표현식"임을 나타낸다.
- /우리가 찾고자하는 패턴/
- /regex/i
- i는 어떤 옵션에 따라 검색할건지 플래그를 활용할 수 있다.

# 문법
1) Groups anf ranges
   - |  : 또는 ![image](https://github.com/leegowoon/regex/assets/145514701/80f8d1f0-26f2-483b-8acd-f451ddac2e12)

   - () : 그룹 ![image](https://github.com/leegowoon/regex/assets/145514701/8203b2c3-9990-4186-9ad4-fd772f1422bf)

   - [] : 문자셋, 괄호안의 어떤 문자든
   - gr로 시작하고 중간글자가 e 또는 a가 되고 y로 끝나는 것을 찾음   
   ![image](https://github.com/leegowoon/regex/assets/145514701/852d6c09-1be1-4559-b382-92f125a916c4)

   
   - [^] : 부정 문자셋, 괄호안의 어떤 문자가 아닐 때 ex) [^a] : a가 아니다.
   
   - (?) : 찾지만 기억하지는 않음
   - 찾아는 지지만 그룹으로 만들고 싶지 않다면 사용  
  ![제목 없음](https://github.com/leegowoon/regex/assets/145514701/8fd32774-2127-4958-bb24-4b1fef3dc3dc)

   - gr로 시작하고 a 또는 e 또는 d가 있고 y로 끝남   
   ![image](https://github.com/leegowoon/regex/assets/145514701/b4ed1a62-935d-4516-bb26-b6defef14bfc)

   - [aed] : 대괄호안에 있는 글자 중 하나라도 만족하는 것을 찾아라  
   ![image](https://github.com/leegowoon/regex/assets/145514701/470ee153-7590-497a-abff-6592cf5a9c91)
   - 아래 두 이미지는 gr로 시작하고 a~g사이의 글자 중 하나라도 포함되고 y로 끝나는 것을 찾음   
   ![image](https://github.com/leegowoon/regex/assets/145514701/fa481ccd-6e29-45e9-8f10-794165bff5a6)
   ![image](https://github.com/leegowoon/regex/assets/145514701/6c598e3c-ac6f-4747-8ac3-3b11883ca8b7)

   - a 부터 z까지, A 부터 Z까지, 0 부터 9까지 하나라도 만족하면 모두 찾는다.(특수문자X)
   ![image](https://github.com/leegowoon/regex/assets/145514701/31f80819-23bc-4148-ae96-cd7cde0cfc9d)

   - ^는 부정의 의미   
   ![image](https://github.com/leegowoon/regex/assets/145514701/ac61c8f3-959d-4ca3-b806-6ae2fe58fb00)

2) 제한하기위해 사용하는
   - ? : 없거나 있거나(zero or one)
   - ' * ' : 없거나 있거나 많거나(zero or more)
   - ' + ' : 하나 또는 많거나(one or more)
   - {n} : n번 반복
   - {min} : 최소
   - {min,max} : 최소 그리고 최대

3) 경계에 대한
   - \b : 단어경계
   - \B : 단어경계가 아닌 것
   - ^  : 문장의 시작(대괄호 밖에 있는 것)
   - $  : 문장의 끝
  
4) 특징을 이용하는 방법
   - \  : 특수문자가 아닌 문자
   - .  : 어떤 글자(줄바꿈 문자 제외)
   - \d : 숫자
   - \D : 숫자가 아닌 것
   - \w : 문자
   - \W : 문자가 아닌 것
   - \s : 공백(space)
   - \S : 공백이 아닌 것


  

---
- multiline : 라인한줄안에서 찾아라
- ![image](https://github.com/leegowoon/regex/assets/145514701/2b36fa85-a52f-4983-8edf-f4c244c59abc)

