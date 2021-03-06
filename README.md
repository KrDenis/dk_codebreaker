# DkCodebreaker

[![Gem Version](https://badge.fury.io/rb/dk_codebreaker.svg)](https://badge.fury.io/rb/dk_codebreaker)
[![Build Status](https://travis-ci.org/DenKey/dk_codebreaker.svg?branch=master)](https://travis-ci.org/DenKey/dk_codebreaker)


Codebreaker is a logic game in which a code-breaker tries to break a secret code created by a code-maker.The code-maker, which will be played by the application we’re going to write, creates a secret code of four numbers between 1 and 6.

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'dk_codebreaker'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install dk_codebreaker

## Quick documentation

```ruby
# create game instance, it get user name and attempts
game = DkCodebreaker::Game.new(name,attempts)

# mandatory run, this will generate secret code
game.start

# set attempts score to nil and regenerate it
game.restart

# enter user answer as string
# Return [position_number String]
# Win if you get "++++" here 
# Error codes:
### :less_then_four
### :guess_has_symbol
### :code_not_string
### :you_lose
game.guess user_code

# return [hint String] 
game.hint

# Return Hash with user data {player,result,attempt,attempts,time}
# :player   - username
# :result   - last game result
# :attempt  - current attempt number
# :attempts - limitation of trying
# :time     - "%m/%d/%Y/%H/%M"
game.user_data

# Getters and Setters 
game.hint_status
game.attempt
game.player
game.player=
game.attempts
game.attempts=
```


## Implementations
[codebreaker_console](https://github.com/DenKey/codebreaker_console)

[codebreaker_web](https://github.com/DenKey/codebreaker_web)

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/DenKey/dk_codebreaker


## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).

