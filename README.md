# Common gems

Just some common gems I use in every Ruby project.

## Usage

First add common-gems as a Git submodule to your project:

```
git submodule add https://github.com/krautcomputing/common-gems.git
```

then you can load the included Gemfiles.

### Rails

For a Rails project add this to your project's Gemfile:

```ruby
%w(
  rails
  redis         # optional
  sidekiq       # optional
  testing       # optional
).each do |module|
  instance_eval(File.read(File.join('common-gems', module, 'Gemfile'))
end
```

Make sure to define the `rails` dependency in the Gemfile **before** the common gems Gemfiles since some common gem versions depend on the required Rails version.

### Middleman

For a [Middleman](http://middlemanapp.com/) project add this to your Gemfile:

```ruby
instance_eval(File.read('common-gems/middleman/Gemfile'))
```
