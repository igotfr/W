## Comments [REVIEW]
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
#### Casting [REVIEW]
```v
i64_123
u8_42
f32_45.7
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
#### Initialization [REVIEW]
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
## Data
```v
strun Person {
   id u32
   name stru8 [named] | cpf u16,
}

p1 := Person{1, name: 'Valdinei'}
p2 := Person{2, 11111111}
```
## Control Structure
### match (exhaustive)
```v
match x, y {
   (2, 3, 7..12, >= 19) && (4, 6, 11.=15, < 0) {}
   (2, 3, 7..12, >= 19) || (4, 6, 11.=15, < 0) {}
}
```
