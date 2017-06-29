# Declaration

## MSDN
https://msdn.microsoft.com/ko-kr/library/dsyxx40f.aspx

## Declaration
```
declaration-specifiers init-declarator-listopt;
```

## declaration-specifiers
```
storage-class-specifier
type-specifier
type-qualifier
```
- storage-class specifier : https://msdn.microsoft.com/ko-kr/library/w9hwbe3d.aspx
  - auto
  - register
  - static
  - extern
  - __declspec /* Microsoft 전용 */
- type-specifier : https://msdn.microsoft.com/ko-kr/library/a86zba5c.aspx
  - void
  - char
  - (signed, unsigned) short, int, long
  - float, double
  - struct, union
  - enum
  - typedef-name
- type-qualifier : https://msdn.microsoft.com/ko-kr/library/888bfst6.aspx
  - const
  - volatile

## init-declarator-list
```
declarator  =  initializer
```
- declarator : https://msdn.microsoft.com/ko-kr/library/e5ace6tf.aspx
  - pointer
  - direct-declarator

### 복잡한 선언자 해석
https://msdn.microsoft.com/ko-kr/library/1x82y1z4.aspx

### 초기화
- 스칼라 : https://msdn.microsoft.com/ko-kr/library/0x80hh2d.aspx
- 집합체 : https://msdn.microsoft.com/ko-kr/library/81k8cwsz.aspx
- 문자열 : https://msdn.microsoft.com/ko-kr/library/7w7xccx8.aspx
