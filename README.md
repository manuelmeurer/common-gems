# Common gems

Just some common gems I use in every Ruby project.

## Usage

First add common-gems as a Git submodule to your project:

```
git submodule add https://github.com/manuelmeurer/common-gems.git
```

then you can load the included Gemfiles.

### Rails

For a Rails project add this to your project's Gemfile:

```ruby
%w(
  rails
  redis            # optional
  sidekiq          # optional
  testing-basics   # optional
  testing-minitest # optional, requires testing-basics, mutually exclusive with testing-rspec
  testing-rspec    # optional, requires testing-basics, mutually exclusive with testing-minitest
).each do |m|
  eval_gemfile File.join('common-gems', m, 'Gemfile')
end
```

Make sure to define the `rails` dependency in the Gemfile **before** the common gems Gemfiles since some common gem versions depend on the required Rails version.

### Middleman

For a [Middleman](http://middlemanapp.com/) project add this to your Gemfile:

```ruby
eval_gemfile 'common-gems/middleman/Gemfile'
```
