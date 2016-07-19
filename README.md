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
