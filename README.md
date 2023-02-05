# rust-cheatsheet
* https://cheats.rs/

## match expression
* Controls the flow of execution based on the value of a variable.
* Allows you to compare a value of a variable against a number of different patterns and execute different code based on which pattern matches 

``` rust
match variable {
    pattern_1 => expression_1,
    pattern_2 => expression_2,
    ...
    pattern_n => expression_n,
}

let value = 3;

match value{
    1 => println!("one");
    2 => println!("Two");
    3 => println!("Three");
    _ => println!("other");
}
```
* The _ pattern is a catch-all that matches any value that doesn't match any of the other patterns.

* How match can be used to destruct enum, struct and tuples
 * struct
 ```
enum Message {
    Quit,
    Move { x: i32, y: i32 },
    Write(String),
    ChangeColor(i32, i32, i32),
}

let message = Message::Move { x: 3, y: 4 };

match message {
    Message::Quit => println!("The program is quitting"),
    Message::Move { x, y } => println!("Moving to ({}, {})", x, y),
    Message::Write(text) => println!("Writing message: {}", text),
    Message::ChangeColor(r, g, b) => println!("Changing color to RGB({}, {}, {})", r, g, b),
}
// The match expression is used to compare the variant of the message value and execute the appropriate code based on the variant that is present.

// 
```

