Piques from ruby 
=================

`ruby for sysAdmins`,`beginning ruby` ,`why_guide` , `Learn ruby the hardWay`, and more.. 

```ruby
#Piques form: Practical Ruby for System Administrators'
# the insane hacker way. 

#inline ruby (insane)
ruby -e 'a = gets.chomp; puts a'
echo 'a = gets.chomp; puts a' > foo.rb
#interpretate file, and show some warnings
ruby -w foo.rb

#every body in ruby is an Object

puts "hello world"              #the implicit way
Kernel.puts.self "hello world"  #the explicit way, Kernel is the superclass

#the puts method is defined on IO class 
# with global objects for unix file-handles:
# $stdin, for standard input
# $stdout, for standard output
# $stderr, for standard error
# $ is for Global 

stderr.puts "Some bug issue"

### Method definition
#Hack fun, an implementation of puts

def puts(f)
	$stdout.puts("hello",f)
end
puts "folks!" 					#Override the kernel puts method, sweet ah?

# hello
# folks
#the same but without brackets
def puts word
	$stdout.puts "hello", word
end
puts "folks!" 					#Override the kernel puts method, sweet ah?

# Class definition
class foo
end

#Method declaration
def foo
end

##Define a class  whith a method 
class Why
	def speak
		"chuncky bacon"
	end
end

#use the class for an explicit large way

f_says = Why.new
puts f_says.speak 

#chunky bacon

#implicit short way :
puts Why.new.speak

## Class Definition with data attributes
#initialize method is called with new
#and passes all arguments to initializate,
#@someAttribute is an instance variable 
#@ is for object variable from some class

class Dog
  def initialize meters years
    @size = meters
	@age = years
  end
  
  def grow meters
    @size += meters
  end
  
  def speak
  	if @size < 0.2 then
		"yap"
	elsif @size < 1 then
		"woof woof"
  	else
	    "ROOOOOAAARRRRR!"
	end
  end #end def
  
  def show_age
  	return @age
  end
end

#create a dog and initialize their size

boby = Dog.new 0.3        # instance a new dog , and set size = 0.3
boby.initializate 0.3, 15 # observe the dinamic type
boby.show_age             # 15
boby.speak 			      # "woof woof"
boby.grow 34       
boby.speak 			      # "ROOOOOAAARRRRR!"

## More basics for OOP in ruby
# return and setting variables

class Building
  #some methods here

  def height
  	return @heigth
  end
  
#setting heigth with some external value
  def height meters
  	@heigth = meters
  end
end

e = Building.new
e.heigth = 440		#setting a value
e.heigth 			#override the method and return the value

# But! Its too noisy have to write this all time!!
# for more fun writting code Matz implement Accessor Macros
# What the hack is an Accessor Macro?
# a set of class and methods to wrapp and automatize tasks
# attr_reader, create a getter Method
# attr_writer, create a setter Method 
# attr_accessor, create both methods

class Foobar
 attr_accessor :foo
 attr_accessor :bar
end

f = Foobar.new
f.foo = "The answer of all questions"
f.bar = 42
puts f.foo + f.bar.to_s 

#the answer of all questions 42
#:foo, :bar are symbols for some unique object attribute

### Blocks page 33 ,"Practical Ruby for System Administrators"
```

