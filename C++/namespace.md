# Namespace

네임스페이스는 내부 식별자에 범위를 제공하는 선언적 영역이다

## MSDN

https://msdn.microsoft.com/ko-kr/library/5cb46ksf.aspx

## 사용법
```
#include <iostream>

namespace MyNamespace
{
	int var;
	void func();
	void func2() {
		var++;
	};
}

void MyNamespace::func()
{
	var++;
};

void func()
{
	MyNamespace::var++;
};

int main()
{
	MyNamespace::func();
	MyNamespace::func2();
	func();
	std::cout << MyNamespace::var;
	return 0;
}
```

## using

### using declaration

```
#include <iostream>

using std::cout;
using std::endl;

int main() {
	cout << "Hello world" << endl;
}
```

### using directive

```
#include <iostream>

using namespace std;

int main() {
	cout << "Hello world" << endl;
}
```

## 전역 네임스페이스

main 함수처럼 namespace가 없는 녀석들은 사실 전역 네임스페이스에 포함되어 있다.

namespace가 여러개로 쓰이는 곳에서는 명시적으로 ::func();와 같이 사용할것

## 무명 네임스페이스

무명 인터페이스는 전역 네임 스페이스와 사용법은 같으나 실제로는 컴파일러가 다른 무명 네임스페이스와 충돌이 발생하지 않도록 처리한다.

```
#include <iostream>

namespace
{
	void func() { std::cout << "Hello world"; }
}

int main()
{
	func();
	return 0;
}
```

## 중첩된 네임스페이스와 인라인 네임스페이스(C++ 11)

중첩된 네임스페이스의 경우, 자식 네임스페이스는 부모 네임스페이스의 멤버에 접근이 가능하지만, 그 반대는 불가능하다.

인라인 네임스페이스의 멤버는 부모의 멤버로 처리된다.

```
namespace Parent
{
	namespace Child
	{
		int var;
	}
	//void func() { std::cout << var; } <- 오류 발생
	inline namespace Child2
	{
		int var2;
	}
	void func2() { std::cout << var2; }
}
```
