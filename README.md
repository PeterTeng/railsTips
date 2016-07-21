# Ruby on Rails Tips
A repository to hold all ruby, ruby on rails tips and tricks I find while studying!

## Ruby
For ruby basic tips, checkout [ruby.md](https://github.com/PeterTeng/railsTips/blob/master/ruby.md) in this repository

## Rails

### New project

```shell
$ rails new appName
$ rails new appName --database=postgresql
```

## Files in rails project

```
├── Gemfile
├── Gemfile.lock
├── README.rdoc
├── Rakefile
├── app
│   ├── assets
│   ├── controllers   # Controller
│   ├── helpers
│   ├── mailers
│   ├── models        # Model
│   └── views         # View
├── bin
├── config
├── config.ru
├── db
├── lib
├── log
├── public
├── test
├── tmp
└── vendor
```
### Routing
Inside `/config/routes.rb`

```ruby
root 'static#top'
```

Use only to use specific action(s)

```ruby
resources :books, only: [:index, :show]
```

Scope Routing Rules

```ruby
get 'books/new' => 'books#new'
get 'books/edit/:id' => 'books#edit'
get 'books/undo/:id' => 'books#undo'
```

DRY :point_down:

```ruby
scope controller: :books do
  get 'books/new' => :new
  get 'books/edit/:id' => :edit
  get 'books/undo/:id' => :undo
end
```

DRY :point_down:

```ruby
scope path: '/books', controller: :books do
  get 'new' => :new
  get 'edit/:id' => :edit
  get 'undo/:id' => :undo
end
```

Even more syntactic

```ruby
scope controller: :books do
```

:point_down:

```ruby
scope :books do
```

:point_down:

```ruby
controller :books do
```

#### Path Prefix

```ruby
scope path: '/books' do
scope '/books/' do

# nested implied prefixed paths

scope :books, :archived do
```

#### Namespaces
Will bundle module, name prefix, and path prefix settings into one declaration

```ruby
namespace :admin do
  resources :books
end

namespace :books, :controller => :books do
  get 'new' => :new
  get 'edit/:id' => :edit
  post 'undo/:id' => :undo
end
```

### Model

### Controller

### View

#### HTMl
- ERB
- haml
- slim

#### CSS
- Sass
- Less
