---
title: Rust By Example
published: 2025-09-27
description: 'Learning notes of Rust By Example'
image: ''
tags: [Rust]
category: 'Example'
draft: false 
lang: ''
---

::github{repo="rust-lang/rust-by-example"}

# 1. Hello World

## 1.1 注释

- rust 的普通注释与 C 语言相同
- Hint💡：可以用一种高效的方式来 comment/uncomment 一段代码

```rust
/* 在最前面加一个 slash 就可以 uncomment
println!("1");
println!("2");
println!("3");
// */
```
## 1.2 格式化打印

- `format!`: 类似于 C 语言的 `sprintf`
- `print!`: 类似于 C 语言的 `printf`
- `eprint!`: 输出到标准错误
- 上述函数的末尾加上 `ln` 则添加换行符

常用的格式化方式：
- `{}` 按顺序匹配参数列表：
```rust
println!("first: {}, second: {}", "Alice", "Bob");
```
- `{no}` 可以通过编号匹配列表中的参数
```rust
println!("first: {0}, second: {1}, first: {0}", "Alice", "Bob");
```
- `{name}` 可以通过变量名匹配列表中的参数
```rust
println!("she: {woman}, he: {man}", 
          woman = "Alice", 
          man = "Bob");
```
# 2. 原生类型

标量类型：
- 有符号整数：`i8` ~ `i128` 和 `isize`（指针大小）
- 无符号整数：`u8` ~ `u128` 和 `usize`（指针大小）
- 浮点数：`f32`、`f64`
- `char`：Unicode 类型（4 字节）
- `bool`：`true`、`false`
- 单元类型：空元组 `()`

复合类型：
- 数组：如 `[1, 2, 3]`
- 元组：如 `(1, true, 'a')`

类型标注：
- 常规标注：
```rust
let logical: bool = true;
```
- 后缀标注：
```rust
let integer = 9i32;
```
- 默认类型：
```rust
let default_float = 3.14 // f64
```