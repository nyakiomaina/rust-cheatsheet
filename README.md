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

