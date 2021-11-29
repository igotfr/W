## Comments
```v
// This is a single line comment.
/*
This is a multiline comment.
   /* It can be nested. */
*/
```
## Variables
### Initialization
```v
a u8 :- 1; b u16 :- 2; c u32 :- 3
// or
a u8 @- 1; b u16 @- 2; c u32 @- 3
```
```v
a u8, b u16, c u32 :- u8_1, u16_2, u32_3
a, b, c u8 @- 1, 2, 3
a, b, c u8 $- 1
```
```v
a \- 1, b \- 2, c \- 3 u8 // ?
```
### Assignment
```v
a u8 := 1; b u16 := 2; c u32 := 3
// or
a u8 @= 1; b u16 @= 2; c u32 @= 3
```
```v
a u8, b u16, c u32 := u8_1, u16_2, u32_3
a, b, c u8 @= 1, 2, 3
a, b, c u8 $= 1
```
```v
a \= 1, b \= 2, c \= 3 u8 // ?
```
## W Types
### Primitive types
```v ignore
bool
stri8  stri16  stri32  stri64   stri128
stru8  stru16  stru32  stru64   stru128
i8    i16  i32  i64      i128 (soon)
u8    u16  u32  u64      u128 (soon)
      f16  f32  f64      f128
isize, usize // platform-dependent, the size is how many bytes it takes to reference any location in memory
voidptr // this one is mostly used for C interoperability
any // similar to C's void* and Go's interface{}
```
### Numbers
#### Casting
```v
i64_123
u8_42
f32_45.7
```
#### Base Notation
```v
0b01111011
0o173
0x7B
```
#### _ as separator
```v
1_000_000 // same as 1000000
0b0_11 // same as 0b11
3_122.55 // same as 3122.55
0xF_F // same as 255
0o17_3 // same as 0o173
```
#### Float power of ten
```v
42e1 // 420
123e-2 // 1.23
456e+2 // 45600
```
## Arrays
### Fixed Size Arrays
#### Initialization
```v
arr 3u8 :- 3u8[1 2 3]
// or
arr 3u8 :- u8[1 2 3]
// or
arr 3u8 :- [1 2 3]
// or
arr :- 3u8[1 2 3]
```
### Dynamic Arrays
#### Initialization
```v
arr _u8 :- u8[1 2 3]
// or
arr _u8 :- [1 2 3]
// or
arr :- u8[1 2 3]
// or
arr :- [1 2 3]
```
#### Destructuring
```v
[a, b, c] u8 :- u8[1 2 3]
// a = 1 b = 2 c = 3
```
