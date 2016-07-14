# Ruby on Rails Tips
A repository to hold all ruby, ruby on rails tips and tricks I find while studying!
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

## Rails
