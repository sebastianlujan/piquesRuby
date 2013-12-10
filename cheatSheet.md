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
print "print the stdin without ","new line"  #print the stdin without new line=> nil
print " print the stdin with\n New line"
# print the stdin with
# New line=> nil

puts "This print the stadin with ","new line"
#This print the stdin with
#new line
#=> nil
```

Getting data from standard input
=================================

```ruby
name = gets # sebastian # => "sebastian\n"
name = gets.chomp # sebastian # => "sebastian"
```

Variables
=========
```ruby
a = 50
b = 4.0
c = a < b #false
```

Printing variables
===================
```ruby
puts "there are #{a} bucks in my pocket"
#there are 50 bucks in my pocket
```

Types and convertion
=====================
```ruby
a,b = 42,2
Integer(a)
Float(b)         # 2.0
Integer(12.5712) # 12
Float(b)         # 2.0
Integer(0xff)    # to hexa
Integer(010)     # to octal
Integer(0b1110)  # to binary
```
```ruby
num = gets.chomp
num.to_i() + 4  # to integer
num.to_f()      # to float
num.to_s()      # to string
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
