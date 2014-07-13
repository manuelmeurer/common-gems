# Common gems

Just some common gems I use in every project.

## Usage

First add common-gems as a Git submodule to your project:

```
git submodule add https://github.com/krautcomputing/common-gems.git
```

then add this to your project's Gemfile:

```ruby
%w(
  common-gems/Gemfile
  common-gems/redis/Gemfile         # optional
  common-gems/sidekiq/Gemfile       # optional
).each do |gemfile|
  instance_eval(File.read(gemfile))
end
```

Make sure to require `rails` before the common gems since some common gem versions depend on the required Rails version.
