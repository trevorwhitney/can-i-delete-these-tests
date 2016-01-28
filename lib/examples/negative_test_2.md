```ruby
describe '/number_generator' do
  it 'returns 200 status code' do
    get '/number_generator'
    expect(last_response).to be_ok
  end

  it 'does not returns 3' do
    get '/number_generator'
    expect(last_response.body).to_not eq '3'
  end
end
```

Note: we could negatively test what our app does not do infinitely