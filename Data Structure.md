# 자료구조란

정보통신기술의 발달에 따라 발생하는 방대한 자료를 효율적으로 관리하기 위해 필요한 것으로 **자료들을 정리하고 조직화하는 구조**이다.

이 때 구조는 각 원소들 사이의 관계가 논리적으로 정의되어 일정한 규칙에 의하여 나열되며 자료에 대한 처리를 효율적으로 수행할 수 있도록 구성되어있다.

![](http://cfile3.uf.tistory.com/image/99820A375C4BB1DD3246B7)

자료구조의 전체 분류를 보자면 위와 같다.

### 선형구조는

![](http://cfile8.uf.tistory.com/image/99F5C14C5C4BB4FC34D074)

**자료들이 순서적으로 나열된 것**을 말하며 데이터에 접근하기 위해 순서접근 또는 직접접근 방법을 사용한다. 직접 접근 방법으로는 배열이 있으며 순서 접근 방법으로는 연결리스트가 있다.

### 비선형구조는

![](http://cfile28.uf.tistory.com/image/994B513D5C4BB4EC333E3B)

**자료들간에 순서가 아닌 보다 복잡한 연결 방법을 갖는 것**으로 트리와 그래프 등이 이에 해당된다. 비선형 구조의 예시로는 트리형식을 갖는 계층구조나 그래프와 같은 지하철노선도 등이 있다

---

## 1\. 배열

**배열은 여러 개의 동일한 자료형의 데이터를 한꺼번에 만들 때 사용**된다.
배열은 인덱스를 갖고 있어 이를 사용하여 각 항목에 직접접근할 수 있으며, 1차원배열, 2차원배열...등으로 만들 수 있다. 문자열 배열의 경우 마지막에는 끝을 나타내는 '\0'이 있어야한다.

```C++
 //사용방법
 int array[scale] = {1,2,3};
 int array[row][col] ={
                     {1,2,3},
                    {4,5,6}
                    };
```

## 2\. 스택

**스택은 자료의 입출력이 후입선출(LIFO : 가장 최근에 들어온 것이 가장 먼저 사용된다.)의 형태로 일어나는 자료구조**를 말한다.

![](http://cfile2.uf.tistory.com/image/9942F4405C4BB721366EAD)

스택에 저장되는 데이터들을 요소(element)라 하며, 스택의 자료를 꺼내는 것을 pop, 넣는 것을 push라 한다. 스택 내에 아무 자료도 없는 경우는 empty상태이며 스택이 꽉 차서 더 이상 자료를 넣을 수 없는 상태를 full상태라 한다.

## 3\. 큐

![](http://cfile27.uf.tistory.com/image/99E9D04F5C4BB8520A72FA)

**큐는 먼저 들어온 데이터가 먼저 나가는 자료구조**이다.
이를 선입선출(FIFO)라하며, 보통 삽입과 삭제가 이루어지는 front와 rear이 정해져있지만
큐의 자료구조 중의 하나인 덱(deque)은 삽입과 삭제가 front 또는 rear 두 곳에서 일어날 수 있도록 허용한다.

## 4\. 연결리스트

![](http://cfile10.uf.tistory.com/image/997001445C4BB9A9093295)

**연결리스트란 동적으로 데이터 크기를 할당할 수 있는 선형적 자료구조**이다.

이를 통해 스택 뿐만 아니라 큐, 리스트, 덱, 트리 등을 구현할 수 있다. 연결리스트는 노드들의 집합이며, 노드는 데이터필드와 링크필드로 이루어져있다. 첫 데이터필드를 가리키는 포인터를 헤드포인터라하며, 더 이상 연결할 노드가 없는 링크필드의 값은 NULL로 설정함으로써 마지막 노드임을 나타낸다.

## 5\. 리스트

리스트란 집합과는 다르게 **각 항목간에 순서의 개념이 있는 선형 자료구조**이다. 리스트의 경우 스택이나 큐와 다르게 삽입과 삭제가 일어나는 front, rear 제한 없이 임의의 위치에 있는 항목에 대한 연산도 허용한다. 연결리스트와 다른 점이 있다면, 연결리스트는 리스트를 구현하는 방법의 한 형태일 뿐이지만, 리스트는 그 자료구조 자체를 말한다.그 예로 리스트는 배열로도 구현이 가능하다. (220p)

## 6\. 트리

![](http://cfile6.uf.tistory.com/image/99497D505C4BBB933BB3A7)

위의 자료구조들이 선형적이었다면 **트리는 비선형적 자료구조이다. 계층적인 자료를 표현하는데 사용되는 트리는 루트노드와 서브트리로 이루어져있으며, edge로 연결되어있다.**

보통 위의 사진처럼 두 개의 자식 노드를 사용하는 이진트리가 주로 사용된다. 그리고 왼쪽부터 차례대로 모두 채우는 이진트리의 모습을 완전 이진트리라 한다.

## 7\. 그래프

![](http://cfile29.uf.tistory.com/image/991987465C4BBC6708D7D4)

**그래프는 요소들이 서로 복잡하게 연결되어 있는 관계를 표현하는 자료구조**이다.
이는 페이스북의 친구 관계를 나타낼 때 유용하며, 네비게이션의 최단거리 경로를 찾을 때 사용되기도 한다. 그래프는 정점(노드:node)과 간선(링크:link)의 집합으로 구성되어있으며, 방향성을 고려하지 않은 무방향 그래프, 간선에 방향성이 존재하는 방향 그래프, 간선에 비용이나 가중치가 할당된 가중치 그래프 등이 있다.


---
스택구현해보기 - 백준 문제


Stack Baekjoon 문제풀이 : https://onepinetwopine.tistory.com/39
# 문제

정수를 저장하는 스택을 구현한 다음, 입력으로 주어지는 명령을 처리하는 프로그램을 작성하시오.  
명령은 총 다섯 가지이다.  
push X: 정수 X를 스택에 넣는 연산이다.  
pop: 스택에서 가장 위에 있는 정수를 빼고, 그 수를 출력한다. 만약 스택에 들어있는 정수가 없는 경우에는 -1을 출력한다.  
size: 스택에 들어있는 정수의 개수를 출력한다.  
empty: 스택이 비어있으면 1, 아니면 0을 출력한다.  
top: 스택의 가장 위에 있는 정수를 출력한다. 만약 스택에 들어있는 정수가 없는 경우에는 -1을 출력한다.

### java.util.stack에서 제공하는 라이브러리를 활용하여 문제를 풀었다.

스택 자료구조는 import java.util.stack;에 있고 이는 java documentation에 잘 나와있다.  
![](http://cfile1.uf.tistory.com/image/99F048335C4BCCC40ED98C)

**제공하는 메소드는 push, pop, peek, empty, search 등이 있으며 사용방법은 다음과 같다.**

1.  Stack 객체 만들기 : Stack stack = new Stack<>();
2.  push 함수 : stack.push(데이터); //데이터 자료형 맞춰주어야함
3.  pop 함수 : stack.pop(); //만약 data가 없을 때 pop하면 EmptyStackException 발생
4.  peek 함수 : stack.peek(); // 만약 data가 없을 때 peek EmptyStackException 발생
5.  empty 함수 : stack.empty(); // 비어있으면 true 뭔가 차있으면 false
6.  search 함수 : stack.search(index); //index번째에 있는 element값을 보여준다.

이를 이용하여 java로 풀었다.

```JAVA
import java.util.*;

public class main {

    public static void main(String[] args) {
        Stack<Integer> stack = new Stack<>(); //java.util.Stack으로 제공받는 Stack 라이브러리
        Scanner sc = new Scanner(System.in);

        int num = sc.nextInt();
        String order;
        int data = 0;
        int buffer;
        boolean buffer2;

        for(int i = 0; i < num; i++) {
            order = sc.next(); //한 단어만 받도록 설정!

            switch(order) {
            case "push":
                data = sc.nextInt();
                stack.push(data);
                continue;
            case "pop":
                try {
                     buffer = stack.pop();
                }catch(EmptyStackException e){
                    buffer = -1;
                    }                
                System.out.println(buffer);
                continue;
            case "size":
                System.out.println(stack.size());
                continue;
            case "empty":
                buffer2 = stack.empty();
                if(buffer2 == false) buffer = 0; else buffer = 1;
                System.out.println(buffer);
                continue;
            case "top":
                try {
                     buffer = stack.peek();
                }catch(EmptyStackException e){
                    buffer = -1;
                    }    
                System.out.println(buffer);
                continue;

            }
        }

    }

}

```

# 추가

pop이나 peek의 경우 스택이 비어있을 때 호출할 경우 에러가 발생하기 때문에 try-catch를 사용했다.  
push의 경우 push문자열을 받은 후 숫자를 한 번 더 받으므로 next()함수와 nextInt()를 사용했다.(nextLine은 엔터가 나올때까지 받으므로 X)  
스택 라이브러리를 활용하지않고 스택을 구현하기 위해서는 배열이나 연결리스트를 사용하면 된다. 배열의 경우 스택의 크기가 고정되는 단점이 있어 isFull등의 함수가 필요할 수 있다.


---

# C++ / 배열로 선형자료구조인 스택 구현해보기

```C++ 
#include <cstdio>
#include <cstdlib>
using namespace std;

const int arraySize = 20;

class Stack{

	int stackData[arraySize];
	int top;
	int displayNum;
	
public:
	
	Stack(){
		top = -1;
		displayNum = 0;
	}
	

	//구현목록 : push / pop / isFull / isEmpty / display
	
	void push(int insertData){
		if(!isFull()){
			stackData[++top] = insertData;}
		else {
			printf("해당 스택은 꽉 차있습니다.\n");
		}
	}

	int pop(){
		if(!isEmpty()){
			return stackData[--top]; }
		else {
			printf("스택이 비어 반환할 것이 없습니다.\n");
			return -999;
		}
	}

	bool isFull(){
		if(top == arraySize-1) return true; else return false;
	}

	bool isEmpty(){
		if(top == -1) return true; else return false;
	}
	

	void display(){
		printf("디스플레이 # 0%d\n",++displayNum);
		for(int i = 0; i <= top; i++)
			printf("%d ",stackData[i]);

		printf("\n");
	}
};

void main(){

	Stack stack;
	for(int i = 0; i < 5; i ++){
		stack.push(i);
	}

	stack.display();

	stack.pop();stack.pop();stack.pop();stack.pop();stack.pop();stack.pop();


	getchar();


}
```
