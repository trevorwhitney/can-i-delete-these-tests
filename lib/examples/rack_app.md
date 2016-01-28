### What is the public api of a Rails app?

A rack app is just a function that takes an environment hash provided by rack, and returns an array
```ruby
require 'rack'

app = Proc.new do |env|
    ['200', {'Content-Type' => 'text/html'}, ['A barebones rack app.']]
end

Rack::Handler::WEBrick.run app
```

So is this the public api of a Rails application?
```ruby
Application.call(env)
```

Note: Why are we testing anything else?