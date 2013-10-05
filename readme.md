# BikeShare
A Ruby gem for interacting with Bay Area Bike Share stations and bike info
* Created by [Zack Shapiro](http://twitter.com/zackshapiro) and [Patrick Traughber](http://twitter.com/ptraughber)

## Installation

```ruby
gem install bikeshare
```

or 

```ruby
require 'bikeshare'
```

## Available methods:


```ruby
response = BikeShare.new
```
Returns the full JSON of stations available and their information

##### `.stations(city_name)`
Takes a city name string such as `"San Francisco"` and returns an array of all the stations in that municipality

##### `.empty_stations`
Returns an array of all stations with 0 `availableBikes`

##### `.empty?(station_id)`
Takes a `station_id` as an integer and retuns true or false based on the number of `availableBikes`

##### `.available_bikes(station_id)`
Takes a `station_id` as an integer and returns the nunber of available bikes

##### `.offline_stations`
Returns an array of stations currently offline

* For more information, please go to the [Bay Area Bike Share website](http://bayareabikeshare.com)
