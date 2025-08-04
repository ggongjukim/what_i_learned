## 백준 JAVA 입출력 세팅방법
```java
import java.io.BufferedReader; 		// BufferedReader import
import java.io.InputStreamReader;	// InputStreamReader import

public class Main {

    // Exception 처리
    public static void main(String[] args) throws Exception {

    	// BufferedReader 선언
    	BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        // BufferedReader를 사용한 입력
        int len = Integer.parseInt(br.readLine());

        br.close();
    }
}
```
## JAVA 문법
- `.toCharArray()` : 문자열을 char 배열로 변환하는 메서드
- `.charAt(숫자)` : 문자열에서 특정 위치의 문자 하나를 가져올 때 사용하는 메서드
-  `StringBuilder` 문자열을 효율적으로 누적하거나 조작할 때 사용하는 객체를 만드는 코드 `append`, `toString` 등. java.lang 패키지에 포함 import 필요없음
