Mutable variable x is bound to a new instance of String: let mut x = String::new()
Associated function x is implemented on type T rather than on an instance of T, like a static function in C++.
Result type is an enum or enumeration. 
Enum X has variants A, B, and C.
A crate is a collection of souce code files
You can depend on other library crates
Cargo update will upgrade dependencies to newer major and minor releases not just patch releases. 
Cargo build will only upgrade dependencies to newer patch releases.
This match as three arms, the pattern for the first arm is the unit type, that makes no sense.
Variable x is shadowed here. let mut x = String::from_str("hello"); let x = x + " World!"; The first x was shadowed by the second x variable. They are different variables.
The type of a const must be annotated. When declaring constants it must be of the form const x: i32 = 42; The : i32 is the type annotation and the type annotation is not optional
A match expression must be exhaustive. Every possible value must match an arm.


Traits Commonly Implemented
std::cmp::Ordering this is an enum. 

Quiz:
In a loop, how do you ignore an error returned in a Result from a function and continue the loop instead?

let mut mystr = String::new();
loop {
  io:stdin::read_line(&mut mystr)?;
  let x: u32 = match mystr.parse() {
    Ok(num) => num,
    Err(_) => continue,
  };
};
  
What are the four primary scalar types in Rust?
integers, floating-point number, booleans, and characters.

How many bytes in a Rust char?
Four bytes represending a Unicode Scalar Value.

What does it mean that Rust is a statically typed language?
It means that the data type of every value is known at compile time.

When would you use a usize?
Indexing a collection is one example

What type do integers default to in Rust?
i32, because even on 64bit machines i32 are slightly faster.

What type do floating point number default to in Rust?
f64, because on modern machines f64 are as fast as f32 and have higher precision.

What is destructuring?
Breaking down a structure into its component parts. For example let (a,b,c) = x; destructured the tuple x into its three items.

When would you use an array instead of a Vector?
Arrays are always allocated on the stack. When the values in the array don't change (much).
