# Ruby Notes

> Use 'puts' to print

> Use '#{var_name}' to inject vars into strings
current_president = "Barack Obama"
puts "In 2016, the president was #{current_president}."

> use_snake_case notCamelCase
There is strong convention among Rubyists to use what is known as snake case this_is_an_example_of_snake_case words are seperated by underscores. This is opposed to camel case thisIsAnExampleOfCamelCase where upcased characters indicate word breaks.

> Vars can't start with a number, include punctuation, or spaces
A Ruby variable cannot start with a number, be a Ruby reserved word, or have punctuation or space characters.

> You can change the data type of a var on command
Ruby is what is known as a dynamically typed language.

> Uses dot notation
Ex: str.upcase, str.downcase, str.length, str.reverse

> Pass by value not refrence language

> Two types of numbers
1) Fixed nums/whole numbers
2) floats (round down to nearest whole int .floor | .round to nearest whole num up or down | .ceil road up to nearest whole int)

> Array syntax
["hello", "world"]

> Hash syntax (HashMap in Java)
{"hello" => "world", "orange" => "peal"}
Hash.new | To set custom return on non-existant key: Hash.new(arg) or hash_name.default = arg
to access values in a hash: hash_name[hash_key]

> A symbol is a representation of a piece of data represented with a : before the identifier.

> Use .class to get the data type of a var