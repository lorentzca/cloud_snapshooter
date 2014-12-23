# CloudSnapshooter

Create cloud snapshot.

[![Gem Version](https://badge.fury.io/rb/cloud_snapshooter.svg)](http://badge.fury.io/rb/cloud_snapshooter)

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'cloud_snapshooter'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install cloud_snapshooter

## Usage

### Amazon EC2

Export environment variable

```bash
$ export AWS_ACCESS_KEY=XXXXXXXX
$ export AWS_SECRET_KEY=YYYYYYYY
$ export AWS_REGION=ZZZZZZZZ
```

Create ec2 volume snapshot

```ruby
require 'cloud_snapshooter'

CloudSnapshooter::Shoot.ec2_snapshot('vol-xxxxxxxx','description')
#=> <AWS::EC2::Snapshot id:snap-yyyyyyyy>
```

Executable commands

```bash
$ cloudsnapshooter ec2 vol-xxxxxxxx description
```

Or

```bash
$ bundle exec ruby cloudsnapshooter ec2 vol-xxxxxxxx description
```

## Contributing

1. Fork it ( https://github.com/Lorentzca/cloud_snapshooter/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
