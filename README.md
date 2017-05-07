# Ruby Notes

## Useful Commands

`irb` to start the ruby interpreter

### General

| Command | Use | Java Equivalent |
| --- | --- | --- |
| `puts arg` | print something to the console | `System.out.print(arg);`
| `#{arg}` | insert a var into a string | `String.fomat(str,insert);`
| `.length` | gets how big or long something is | Same
| `.reverse` | reverses the order of something | `new StringBuilder(str).reverse().toString();` & `ArrayUtils.reverse(array);`
| `.new` | empty instantiation | `new` keyword
| `.new(arg)` | instantiation | `Type name = arg;`
| `.class` | get the data type of a var | `.getClass().getSimpleName();`


### String Class

| Command | Use |
| --- | --- |
| `.upcase` | convert str to all upper case |
| `.downcase` | convert str to all lower case |

### Float Class
- Any number with a decimal is called a Float

| Command | Use |
| --- | --- |
| `.ceil` | round _up_ to nearest whole int |
| `.round` | round _up or down_ to nearest whole int |
| `.floor` | round _down_ to nearest whole int |

### Arrays
- It is possible to create an array that contains different data types, but that is generally discouraged.
- Elements are accessed via index; the first element is at index 0.

| Command | Use |
| --- | --- |
| `<<` | Shovel Operator: Adds _an_ element to the _end_ of an array
| `.push(args)` | same as the Shovel Operator, but can _add multipal elements_
| `.unshift(args)` | to _add elements_ to the _front_ of an array
| `.inspect` | returns the array as a String
| `.shift` | removes and returns the first item
| `.pop` | removes and returns the last element
| `.include?(arg)` | checks if the array contains an element
| `.sort` | sorts the array

## General Notes
- Ruby uses_snake_case, unlike Java's camelCase
- Var names can't start with a number, have punctuation, be a reserved Ruby keyword, or include a space
- Dynamically Typed Lang: Data types of vars change as needed
- Uses dot notation like Java
- Passes by value, not refrence
- A whole number is called a fixed number (Fixnum)
- A symbol is a representation of a piece of data represented with a : before the identifier. They refer to an area of memory; this is different from, for example, strings, which take up new areas of memory every time they are used.

### Hash Class Notes
- Example of syntax: `{"hello" => "world", "orange" => "peal"}`
- Values are accessed from the key. Ex: `hash_name[key]` returns the value associated to the key
- `Hash.new(arg)` or `.default = arg` is used to set what is returned when attempting to access a non-existant key
- HashMap is the Java equivalent
