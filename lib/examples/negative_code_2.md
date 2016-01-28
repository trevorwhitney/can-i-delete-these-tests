__GIVEN__ I request a randomly generated number

__THEN__ I don't get a 3

```ruby
require 'sinatra'

get '/number_generator' do
end
```