```ruby
describe '/number_generator' do
  it 'returns 200 status code' do
    get '/number_generator'
    expect(last_response).to be_ok
  end

  it 'returns 3' do
    get '/number_generator'
    expect(last_response.body).to eq '3'
  end
end
```