Command parameters
===================

```bash
foo.rb
ruby foo.rb
ruby -e 'expresion'
ruby -w foo.rb #interpret the foo.rb and show warnings
irb #the Interactive Ruby Shell
```

puts vs print
==============
```ruby
print "This print the standard input without ", "new line"
#This print the standard input without new line=> nil

print " This print the standard input with\n New line"
# This print the standard input with
# New line=> nil

puts "This print the standard input with ", "new line"
#This print the standard input with
#new line
#=> nil
```

Getting data from standard input
=================================

```ruby

name = gets # sebastian # => "sebastian\n"
name = gets.chomp # sebastian # => "sebastian"

```

Types and convertion
=====================
```ruby
a = "42"
Integer(a)
Integer(12.5712) # 12
Integer(0xff)    # to hexa
Integer(010)     # to octal
Integer(0b1110)  # to binary
```
```ruby
num = gets.chomp
num.to_i() + 4  # to integer
num.to_f()      # to float

```

Strings
========
```ruby
a = "foobar" # "foobar"
quote = <<foo
a large quote of text
more text
a little bit more
ok its enough
foo
print(quote)
```







Methods
========

```ruby
def square(n)
   return n * n
end
```
