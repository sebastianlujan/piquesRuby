command parameters
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

puts "This print the standard input with ", "new line"
#This print the standard input with
#new line
#=> nil
```


methods
========

```ruby
def square(n)
   return n * n
end
```
