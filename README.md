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

equals to

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

## Rails
