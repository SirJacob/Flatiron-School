# Ruby Notes

## Useful Methods

### General

| Method | Use | Java Equivalent |
| --- | --- | --- |
| `#{arg}` | insert a var into a string | `String.format(str,insert);`
| `.length` | gets how big or long something is | Same
| `.reverse` | reverses the order of something | `new StringBuilder(str).reverse().toString();` & `ArrayUtils.reverse(array);`
| `.new` | empty instantiation | `new` keyword
| `.new(arg)` | instantiation | `Type name = arg;`
| `.class` | get the data type of a var | `.getClass().getSimpleName();`

### Console

| Method | Use | Java Equivalent |
| --- | --- | --- |
| `puts arg` | print something to the console _with_ a new line | `System.out.println(arg);`
| `print arg` | print something to the console _without_ a new line | `System.out.print(arg);`
| `gets` | recieve input from the console | `new Scanner(System.in);`

### String Class
- You can use the `==` operator to compare two strings; unlike Java's `.equals(str)`

| Method | Use |
| --- | --- |
| `.upcase` | convert str to all upper case |
| `.downcase` | convert str to all lower case |
| `.strip` | removes both _trailing whitespace and new lines_
| `.chomp` | removes _new lines_ at the end of the str

### Fixnum Class
- Any whole number is called a Fixed Number

| Method | Use |
| --- | --- |
| `.even?` | checks if the number is _even_
| `.odd?` | checks if the number is _odd_

### Float Class
- Any number with a decimal is called a Float

| Method | Use |
| --- | --- |
| `.ceil` | round _up_ to nearest whole int |
| `.round` | round _up or down_ to nearest whole int |
| `.floor` | round _down_ to nearest whole int |

### Arrays (Collections)
- It is possible to create an array that contains different data types, but that is generally discouraged.
- Elements are accessed via index; the first element is at index 0.

| Method | Use |
| --- | --- |
| `<<` | Shovel Operator: Adds _an_ element to the _end_ of an array
| `.push(args)` | same as the Shovel Operator, but can _add multiple elements_
| `.unshift(args)` | to _add elements_ to the _front_ of an array
| `.inspect` | returns the array as a String
| `.shift` | removes and returns the first item
| `.pop` | removes and returns the last element
| `.include?(arg)` | checks if the array contains an element
| `.sort` | sorts the array

#### Boolean Enumerables
- Loops through the block, updating the var within the pipes to the next element after each execution
- [Breakdown of Boolean Enumerables](https://learn.co/lessons/ruby-boolean-enumerables)

`.all?` returns true if _all_ of the iterations returned `true`
```ruby
[1,3].all? { |number| number.odd? } #=> true
```

`.none?` returns true if _none_ of the iterations returned `true`
```ruby
[1,3].none? { |i| i.even? } #=> true
```

`.any?` returns true if `any` of the iterations returned `true`
```ruby
[1,2,100].any? { |i| i > 99 } #=> true
```

#### Search Enumerables
- [Breakdown of Search Enumerables](https://learn.co/lessons/ruby-search-enumerators)

## Notes

### General
- Ruby uses_snake_case, unlike Java's camelCase
- Var names can't start with a number, have punctuation, be a reserved Ruby keyword, or include a space
- Dynamically Typed Language: Data types of vars change as needed
- Uses dot notation like Java
- Passes by value, not reference
- A symbol is a representation of a piece of data represented with a : before the identifier. They refer to an area of memory; this is different from, for example, strings, which take up new areas of memory every time they are used.
- Everything is default true. Exceptions include `nil` and `false`

### Hash Class
- Example of syntax: `{"hello" => "world", "orange" => "peal"}`
- Values are accessed from the key. Ex: `hash_name[key]` returns the value associated to the key
- `Hash.new(arg)` or `.default = arg` is used to set what is returned when attempting to access a nonexistent key
- HashMap is the Java equivalent

### Methods
- Using the `return` keyword stops execution of the method and returns the var
- Any var on the last line of a method has an _implied `return` statement_
- Vars created inside a method are disposed of after the method ends and are only accessible from inside the method
- Methods that return `true` or `false` have identifiers that end with a `?` (convention). Ex: `.include?(arg)`

Example of method declaration syntax:
```ruby
def greeting(output) #Method Identifier and Argument Identifiers
  puts output #Method Body
end #Method Closing
```

#### Optional Arguments
- It is conventional to place any default arguments at the end of an argument list when defining a method that takes in both required and default arguments.

Example of syntax:
```ruby
def greeting(name, language="Ruby")
  puts "Hello, #{name}. We heard you are a great #{language} programmer."
end
```

#### Calling Methods
- Can be called just by typing its identifier like a var
- Their identifiers are references to blocks of code (:method_name)

Calling methods that _don't_ accept an arg: `method_name` or `method_name()`

Calling a method that _does_ accept args: `method_name(args)`

### Loops

#### Enumerated Loop:
- Loops the block a set number of times
```ruby
x = 1
3.times { x = x + 1 } #x => 4

# or using the `do` and `end` keywords
x = 1
3.times do
	x = x + 1 #x => 4
end 
```

#### Infinite Loop:
- Loops forever. Use `break` to break out of the loop
```ruby
loop do
  puts "Forever!"
end
```

#### While Loop:
```ruby
- Loops while the condition is false.
x = 0
while x < 4
  x += 1 #x => 4
end
```

#### Until Loop:
- Loops until the condition is true.
```ruby
x = 0
until x == 4
  x += 1 #x => 4
end
```

#### Each Loop:
- Interates through the array and sets the var color to each color stored in the array
```ruby
colors = ["Red", "Yellow", "Blue"]
colors.each do |color| # | | are called _pipes_
  puts "Color #{color} is #{color.length} letters long."
end
```

### RSpec
- A testing tool used to test your Ruby code.
- `rspec --fail-fast` flag is used to stop testing after the first failure
- [Breakdown of RSpec](https://learn.co/lessons/rspec-fizzbuzz)

## Terminology

| Term | Meaning |
| --- | --- |
| Command Line Applications or Interface | programs that you interact with solely from the terminal/shell
| gem | a library of code implemented to add functionality |
| shebang line | Nickname for the line that tells the shell which interpreter to use. Ex: `#!/usr/bin/env ruby`
| double-bang operator | Nickname for the use of a double not. Ex: `!!true` => true
| edge case | refers to scenarios that might occur and we can anticipate, but that are unlikely to be the norm
| helper method | handles a discrete unit of behavior and is used inside of other methods to carry out a larger task


### Reserved/Keywords

| Keyword | Use |
| --- | --- |
| `elsif` | Java equivalent of `else if`
| `def` | used to _define_ methods
| `end` | used to end structures. Java equivalent of `}`
| `break` | stops executing the inner-most loop


### Folders

| Location | Purpose |
| --- | --- |
| `bin/` | Binary: contains executable files to run the program
| `config/` | Configeration: code required to initialize the environment
| `lib/` | Library: code containing methods and classes
| `spec/` or `test/` | Tests: code used to run tests