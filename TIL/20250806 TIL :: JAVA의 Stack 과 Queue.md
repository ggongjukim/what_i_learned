### JAVA Stack
- `import java.util.Stack;`
- Java 표준 라이브러리의 컬렉션 프레임워크 중 하나이다.
- LIFO(Last-In-First-Out) 원칙을 따르는 스택 자료구조를 구현한 클래스입니다.
- 내부적으로 벡터(Vector)를 상속받아 구현되어 있다.
```JAVA
import java.util.Stack;

public class Main {
    public static void main(String[] args) {
        Stack<Integer> stack = new Stack<>();

        stack.push(10);
        stack.push(20);
        System.out.println(stack.peek());  // 20 출력
        System.out.println(stack.pop());   // 20 제거 후 출력
        System.out.println(stack.empty()); // false 출력 (아직 10이 남아있음)
    }
}

```

#### 주요 메서드
 | 메서드                | 설명                     |
| ------------------ | ---------------------- |
| `push(E item)`     | 스택의 맨 위에 요소를 추가        |
| `pop()`            | 스택의 맨 위 요소를 제거하고 반환    |
| `peek()`           | 스택의 맨 위 요소를 제거하지 않고 반환 |
| `empty()`          | 스택이 비어있는지 확인 (boolean) |
| `search(Object o)` | 스택에서 객체 위치를 반환         |


<br/>
<br/>

### JAVA Queue
- Java 컬렉션 프레임워크의 인터페이스(interface) 중 하나로, FIFO(First-In-First-Out) 자료구조를 나타낸다.
- Queue는 인터페이스이기 때문에 직접 인스턴스를 만들 수 없고, 이를 구현한 클래스(예: LinkedList, PriorityQueue, ArrayDeque 등)를 사용해야 한다.
```JAVA
import java.util.Queue;
import java.util.LinkedList;

public class Main {
    public static void main(String[] args) {
        Queue<Integer> queue = new LinkedList<>();

        queue.offer(10);
        queue.offer(20);

        System.out.println(queue.peek());  // 10
        System.out.println(queue.poll());  // 10 제거 및 반환
        System.out.println(queue.isEmpty()); // false
    }
}

```

#### 주요 메서드
| 메서드          | 설명                                  |
| ------------ | ----------------------------------- |
| `add(E e)`   | 큐에 요소를 추가 (가득 찼을 때 예외 발생)           |
| `offer(E e)` | 큐에 요소를 추가 (가득 찼을 때 `false` 반환)      |
| `poll()`     | 큐에서 앞 요소를 꺼내고 제거 (비어 있으면 `null` 반환) |
| `remove()`   | 큐에서 앞 요소를 꺼내고 제거 (비어 있으면 예외 발생)     |
| `peek()`     | 큐에서 앞 요소를 조회만 함 (비어 있으면 `null`)     |
| `element()`  | 큐에서 앞 요소를 조회만 함 (비어 있으면 예외 발생)      |



<br/>
<br/>


### 다른 프로그래밍언어와 Stack, Queue 자료구조 제공 비교
| 언어             | 스택 자료구조 제공 여부                               | 큐 자료구조 제공 여부                     | 비고                        |
| -------------- | ------------------------------------------- | -------------------------------- | ------------------------- |
| **Java**       | `Stack`, `Deque` 등 제공                       | `Queue`, `Deque` 인터페이스 및 구현체 제공  | 스택/큐 전용 클래스, 인터페이스 존재     |
| **Python**     | 전용 Stack 없음, `list`나 `collections.deque` 사용 | `collections.deque` 등 사용         | 리스트로 스택, 덱으로 큐 구현 가능      |
| **C++**        | `<stack>` STL 컨테이너 제공                       | `<queue>`, `<deque>` STL 컨테이너 제공 | 표준 라이브러리(STL)에 있음         |
| **JavaScript** | 전용 스택/큐 클래스 없음, 배열로 구현                      | 배열(Array)로 스택/큐 구현               | 라이브러리 필요 시 직접 구현 또는 외부 사용 |
| **Go**         | 전용 스택/큐 패키지 없음, 슬라이스 활용                     | 슬라이스 및 채널(Channel) 활용            | 직접 구현해야 함                 |

