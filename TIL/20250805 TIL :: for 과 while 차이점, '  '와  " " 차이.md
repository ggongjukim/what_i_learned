### JAVA에서 N개의 입력값이 들어오지만 N이 주어지지 않을때
```Java
  BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
  String line;

  while ((line = br.readLine()) != null && !line.isEmpty()) {
      // 입력된 한 줄 처리
      System.out.println("입력: " + line);
  }
```
### for문과 while문의 차이점
- for문의 초기식	✅ 가능 : `for (int i = 0; i < n; i++)`
- while문의 조건식	❌ 불가능 (변수 선언 불가) : `while ((String line = br.readLine()) != null) ` ❌
- for 문은 초기식, 조건식, 증감식이 한 구문 안에 모여있고, 그 초기식에서 변수 선언도 허용돼서, int i = 0 같이 쓸 수 있다
- 반면에 while 문은 조건식이 단순 boolean 표현식만 가능하고, 변수 선언 구문은 안된다

### 여러 변수 선언 및 초기화
`int a = 0, b = 0;` 이런 식으로 가능하다   
혹은 `int[] arr = {0,0};`    
멤버 변수는 기본값 자동 설정된다   

### 판별 메서드
Character.isLowerCase(char)	소문자인지 판별
Character.isUpperCase(char)	대문자인지 판별
Character.isDigit(char)	숫자인지 판별
Character.isLetter(char)	알파벳인지 판별 (대/소문자 모두 포함)


### Java에서 ' ' 와 " " 차이
- `' '` : char 타입 — 한 글자 문자 리터럴
- `" "` : String 타입 — 문자열 리터럴, 글자 여러 개 가능  

#### System.out.println()에서 공백 출력할 때는?
`System.out.println(a + " " + b + " " + c + " " + d);` " " (String 공백) 써야 한다
왜냐하면 + 연산자가 String과 다른 타입을 만나면 String 연결 연산으로 작동하기 때문이다.    

`System.out.println(a + ' ' + b);` 이 경우, a + ' '는 숫자 덧셈이 돼서, 예상과 다른 결과가 나올 수 있다.

**문자열 연결하려면 항상 " " (문자열 리터럴)로 공백 넣기!**

참고로 '\n' 은?
'\n'은 char 타입 줄바꿈 문자
System.out.println()은 기본으로 줄바꿈 하니까 보통 '\n' 안 넣어도 된다.

다음에는 `System.out.printf` 를 활용해보자
