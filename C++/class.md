# Class

## MSDN
https://msdn.microsoft.com/ko-kr/library/w5c4hyx3.aspx

## 구문
```
Class [tag [: base-list ]] 
{
  member-list
} [declarators];  
[ class ] tag declarators;
```

## 멤버 액세스 제어
기본 액세스는 class에서 private, struct, union에서 public

### MSDN
https://msdn.microsoft.com/ko-kr/library/kktasw36.aspx

### private
클래스의 멤버 함수 및 friend(클래스 또는 함수)에서 사용 가능

### protected
클래스의 멤버 함수 및 friend(클래스 또는 함수), 파생 클래스에서 사용 가능

### public
모든 함수
