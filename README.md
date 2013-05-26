# Buff

Buff is a Buffer API Wrapper written in Ruby.  It provides more thorough API coverage than the existing gem.

Since the gem is currently in ALPHA development, the interface is prone to change.  Please wait until v0.1.0 is released to become reliant on interface. As it stands, all of the basic API calls in BufferApp's spec are available.  Some of the optional params are yet to be implemented.


## Installation

[![Coverage Status](https://coveralls.io/repos/zph/buff/badge.png?branch=master)](https://coveralls.io/r/zph/buff?branch=master) [![Build Status](https://travis-ci.org/zph/buff.png?branch=master)](https://travis-ci.org/zph/buff) [![Code Climate](https://codeclimate.com/github/zph/buff.png)](https://codeclimate.com/github/zph/buff)

Once Buff is released as a gem, the following instructions will work. For now please `git clone` the repo.

Add this line to your application's Gemfile to include HEAD code:

    `gem 'buff', :github => 'zph/buff'`

And then execute:

    `$ bundle`

Or install RubyGems version, which will receive more attention to stability:

    `$ gem install buff`

## Usage

  * Note that some of the optional params are not implemented!
  * All methods are tested with Rspec and WebMock. Most methods do not have integration tests that reach out to the live Buffer API servers.  Proceed with caution until Buff reaches v0.1.0 and submit issues on Github Issues tab.
  * Authentication is not included in this gem (Try OAuth-buffer) or use the single API key given when registering your own Buffer Dev credentials.
  * For convenience load credentials into `~/.bufferapprc` in the following layout.  This allows the `ACCESS_TOKEN` to be loaded into `Buff::ACCESS_TOKEN`:


```
    CLIENT_ID
    CLIENT_SECRET
    ACCESS_TOKEN

    # Structure:
    # client ID line 1
    # client secret line 2
    # Access Token: line 3
```

## API Coverage

#### Implemented

* User
* Profiles (:get, :post)
* Updates (:get, :post)
* Links
* Info
* Error Codes

#### Not Implemented

* Caching
* Various optional params

## Supported Ruby Implementations
- MRI 2.0.0
- Others likely work but are not included in CI Server

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

Issues, refactoring, and feedback are all welcome.

Also, this project is newcomer friendly!! We'd love to be your first Open Source Software contribution and would be happy to assist in that process.

Crafted with care by Zander. Reach out and say hi at [@_ZPH](http://twitter.com/_ZPH) or [civet.ws](http://www.civet.ws)
