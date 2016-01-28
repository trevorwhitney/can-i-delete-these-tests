__GIVEN__ I request a randomly generated number

__THEN__ I receive a 3

```ruby
require 'sinatra'

get '/number_generator' do
  3
end
```