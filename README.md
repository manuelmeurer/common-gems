# Common gems

Just some common gems I use in every project.

## Usage

First add common-gems as a Git submodule to your project:

```
git submodule add https://github.com/krautcomputing/common-gems.git
```

then add this to your project's Gemfile:

```ruby
['common-gems/Gemfile', 'common-gems/rails3/Gemfile'].each do |gemfile|
  instance_eval(File.read(gemfile))
end
```
