## Comments [REVIEW]
```v
// This is a single line comment.
/*
This is a multiline comment.
   /* It can be nested. */
*/
```
## W Types
### Primitive types - Differs on str
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
