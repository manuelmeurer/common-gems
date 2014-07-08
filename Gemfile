# Utils
gem 'pry',                            '~> 0.10', require: false
gem 'awesome_print',                  '~> 1.2',  require: false
gem 'log_buddy',                      '~> 0.7',  require: false
gem 'airbrake',                       '~> 4.0'
gem 'nifty_settings',                 '~> 1.1'
gem 'newrelic_rpm',                   '~> 3.9'
gem 'tries',                          '~> 0.3'
gem 'rack-mini-profiler',             '~> 0.9'

# Services
gem 'services',                       '~> 0.1'

# Postgres
gem 'pg',                             '~> 0.17'

# Redis
gem 'redis',                          '~> 3.1'
gem 'redis-namespace',                '~> 1.5'
gem 'connection_pool',                '~> 2.0'
gem 'redis-rack-cache',               '~> 1.2'

group :development do
  gem 'quiet_assets',                 '~> 1.0'
  gem 'annotate',                     '~> 2.6', require: false
  gem 'better_errors',                '~> 1.1'
  gem 'binding_of_caller',            '~> 0.7' # For better_errors
  gem 'pry-remote',                   '~> 0.1'
  gem 'pry-byebug',                   '~> 1.3'
end

group :development, :test do
  gem 'spring',                       '~> 1.1'
  gem 'spring-commands-rspec',        '~> 1.0'
  gem 'fakeredis',                    '~> 0.5'
end

group :production do
  gem 'puma',                         '~> 2.8', require: false
end
