## Ruby
### Class and Module

Name with camel case

```ruby
class SampleClass
end

module SampleModule
end
```
#### Class
```ruby
class MyClass
  def hello
    puts 'Hello!'
  end
end

my_object = MyClass.new
my_object.hello # => "Hello!"
```

### Method

Name with snake case

```ruby
def sample_method
end
```

```ruby
def hello(names)
  names.each do |name|
    puts "Hello #{name}"
  end
end

languages = ['Ruby', 'Swift', 'Javascript']

hello(languages)
# => "Hello, Ruby", "Hello, Swift", "Hello, Javascript"
```

```ruby
def add(i, k)
  i + k
end

add(5, 4) #=> 9
```

```ruby
def greet(name, message = 'Hi')
  "#{message}, #{name}"
end

greet 'Rails' # => "Hi, Rails"

```

### Block

```ruby
1.upto(5) do |i|
  puts i
end
```

equals to :point_down:

```ruby
1.upto(5) { |i| puts i}
```

### Conditional branching

```ruby
n = 2
if n.zero?
  puts 'is zero'
elsif n.even?
  puts 'is even'
elsif n.odd?
  puts 'is odd'
end
```
### Instance Variable

```ruby
class Ruler
  def length=(val)
    @length = val
  end

  def length
    @length
  end
end

ruler = Ruler.new

ruler.length = 1000
ruler.length #=> 1000
```

Use `attr_accessor` to define same methods :point_down:

```ruby
class Ruler
  attr_accessor :length
end
```

Display the length :point_down:

```ruby
class Ruler
    attr_accessor :length

    def display_length
      puts lenght
    end
end

ruler = Ruler.new
ruler.length = 1000
ruder.display_length # => "1000"
```

#### self

```ruby
class Ruler
    attr_accessor :length

    def set_default_length
      self.length = 1000
    end
end

ruler = Ruler.new
ruler.length = 1000
ruder.set_default_length # => 1000
```

### Class Inheritance

```ruby
class Parent
  def hello_parent
    puts 'Hello, parent!'
  end
end

class Child < Parent
  def hello_child
    puts 'Hello, child!'
  end
end

child = Child.new
child.hello_child    # => "Hello, child!"
chile.hello_parent   # => "Hello, parent!"
```

### Module

```ruby
module Hello
  class Parser
  end
end
module Bye
  class Parser
  end
end
Hello::Parser
Bye::Parser
```

### Hash
Before ruby 1.9
```ruby
colors = {'red' => 'ff0000', 'green' => '00ff00', 'blue' => '0000ff'}
```
After ruby 1.9
```ruby
colors = {red: 'ff0000', green: '00ff00', blue: '0000ff'}
colors[:red]
# or
colors['red']
```

### Range
```ruby
(1..5).include?(5) # => true
(1...5).include?(5) # => false
```

### Object

```ruby
class MyClass
end

MyClass.superclass # => object

obj = Object.new

obj.class            # => Object
obj.is_a?(object)    # => true
obj.object_id        # => 7397828313322
obj.nil?             # => false
obj.frozen?          # => false
```
