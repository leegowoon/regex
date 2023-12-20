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
   ![image](https://github.com/leegowoon/regex/assets/145514701/0068df32-2944-4436-93f0-e34686a7b108)

   
   - [^] : 부정 문자셋, 괄호안의 어떤 문자가 아닐 때 ex) [^a] : a가 아니다.
   
   - (?) : 찾지만 기억하지는 않음
   - 찾아는 지지만 그룹으로 만들고 싶지 않다면 사용  
  ![제목 없음](https://github.com/leegowoon/regex/assets/145514701/8fd32774-2127-4958-bb24-4b1fef3dc3dc)

   - gr로 시작하고 a 또는 e 또는 d가 있고 y로 끝남   
   ![image](https://github.com/leegowoon/regex/assets/145514701/d639baf7-9c6a-4613-acee-5499304f13de)

   - [aed] : 대괄호안에 있는 글자 중 하나라도 만족하는 것을 찾아라  
   ![image](https://github.com/leegowoon/regex/assets/145514701/aafa7fe2-f0ae-4737-a92b-b8fab15c7ec5)

   - 아래 두 이미지는 gr로 시작하고 a~g사이의 글자 중 하나라도 포함되고 y로 끝나는 것을 찾음   
   ![image](https://github.com/leegowoon/regex/assets/145514701/d1c7fdc3-2a1b-4ad0-922c-a31bdcdeb66f)
   ![image](https://github.com/leegowoon/regex/assets/145514701/76fc1403-3d24-4c88-b771-d1151fa124fb)


   - a 부터 z까지, A 부터 Z까지, 0 부터 9까지 하나라도 만족하면 모두 찾는다.(특수문자X)
   ![image](https://github.com/leegowoon/regex/assets/145514701/31f80819-23bc-4148-ae96-cd7cde0cfc9d)

   - ^는 부정의 의미   
   ![image](https://github.com/leegowoon/regex/assets/145514701/ac61c8f3-959d-4ca3-b806-6ae2fe58fb00)

2) 제한하기위해 사용하는
   - ? : 없거나 있거나(zero or one,많거나X)   
   ![image](https://github.com/leegowoon/regex/assets/145514701/872447c4-d85b-4b95-b79b-736ea6a8ae29)

   - ' * ' : 없거나 있거나 많거나(zero or more)   
   ![image](https://github.com/leegowoon/regex/assets/145514701/58c5511e-88fc-412a-804c-f30a53ec208a)

   - ' + ' : 하나 또는 많거나(one or more)   
   ![image](https://github.com/leegowoon/regex/assets/145514701/bea18c96-4ddc-4ee5-a5bf-52230d2e59b3)


   - {n} : n번 반복   
   ![image](https://github.com/leegowoon/regex/assets/145514701/da08cb6c-7c19-46c5-a7a4-4bfcd6e89a9d)


   - {min} : 최소   
   ![image](https://github.com/leegowoon/regex/assets/145514701/aaf6c7cf-e541-4cc1-9083-d6d96949d01e)


   - {min,max} : 최소 그리고 최대   
   ![image](https://github.com/leegowoon/regex/assets/145514701/5e90a60a-1080-4559-ae92-2f0a3eac62ae)


3) 경계에 대한
   - \b : 단어경계
   - /\bYa/ : Ya인데 단어 중에서 Ya로 시작하는 Ya를 찾는다.     
   ![image](https://github.com/leegowoon/regex/assets/145514701/69f8e7c9-1a06-4bc8-b764-dad03919dba3)
   - /Ya\b/ : Ya인데 단어 중에서 Ya로 끝나는 Ya를 찾는다.      
   ![image](https://github.com/leegowoon/regex/assets/145514701/f911317d-5131-4049-a774-0b8b5de2d753)

   - \B : 단어경계가 아닌 것
   - /Ya\B/ : Ya인데 단어 중에서 Ya로 끝나지 않는 Ya를 찾는다.   
   ![image](https://github.com/leegowoon/regex/assets/145514701/e75d2890-a3d4-491a-ae35-768ebe500713)

   - ^  : 문장의 시작(대괄호 밖에 있는 것)
   - /^Ya/ : 문장의 시작인 Ya   
   ![image](https://github.com/leegowoon/regex/assets/145514701/c9e7f847-6455-4cf0-b558-33e6d7d85390)

   - $  : 문장의 끝
   - /Ya$/ : 문장의 끝나는 Ya   
   ![image](https://github.com/leegowoon/regex/assets/145514701/8adb9f3d-6881-473c-a07a-5f0f9b819d67)

  
4) 특징을 이용하는 방법
   - \  : 특수문자
     
   - .  : 어떤 글자(줄바꿈 문자 제외)
   - /./ : 모든 문자   
   ![image](https://github.com/leegowoon/regex/assets/145514701/eb0ad004-d9c2-4ac9-bdfb-f809132c534b)
   - /\./ : 마침표를 찍을려면 역슬래시 사용    
   ![image](https://github.com/leegowoon/regex/assets/145514701/7544e569-88b4-49fd-b338-e4bec0e4340f)

   - []{} 찾을 때   
   ![image](https://github.com/leegowoon/regex/assets/145514701/ae94b7ea-9472-4127-bd80-be5dce1c67bf)

   - \d : 숫자   
   ![image](https://github.com/leegowoon/regex/assets/145514701/b71068b9-3c85-482a-a6d4-8692f75e8d4d)

   - \D : 숫자가 아닌 것   
   ![image](https://github.com/leegowoon/regex/assets/145514701/04adb276-b26e-4eba-a630-8d3e9b76836a)

   - \w : 문자(글자와 숫자)   
   ![image](https://github.com/leegowoon/regex/assets/145514701/ace600a3-aca3-49db-905d-8833b20b3b79)

   - \W : 문자가 아닌 것   
   ![image](https://github.com/leegowoon/regex/assets/145514701/ff1f05c6-6aba-450d-a4e2-3385f6b48fc9)

   - \s : 공백(space)   
   ![image](https://github.com/leegowoon/regex/assets/145514701/b0ef40ce-3e67-4064-9e7f-4532febd1e91)

   - \S : 공백이 아닌 것   
   ![image](https://github.com/leegowoon/regex/assets/145514701/62996022-83eb-4217-b774-12ef9d1086d6)



  

---
- multiline : 라인한줄안에서 찾아라
- ![image](https://github.com/leegowoon/regex/assets/145514701/2b36fa85-a52f-4983-8edf-f4c244c59abc)

