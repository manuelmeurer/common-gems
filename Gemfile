rails = dependencies.detect { |dependency| dependency.name == 'rails' }
raise 'Rails dependency not found, please define before loading common gems.' if rails.nil?
@rails_major_version = rails.requirement.to_s[/\d/, 0].to_i
raise "Could not determine Rails dependency requirement, expected major version 3 or 4 but got #{@rails_major_version}" unless [3, 4].include?(@rails_major_version)

# Basics
gem 'haml-rails',                     @rails_major_version == 3 ? '~> 0.4.0' : '~> 0.5'
gem 'sass-rails',                     @rails_major_version == 3 ? '~> 3.2'   : { github: 'rails/sass-rails' } # TODO: Use this for Rails 4 when sass-rails > 4.0.3 supports sass 3.3: '~> 4.0'
gem 'coffee-rails',                   @rails_major_version == 3 ? '~> 3.2'   : '~> 4.0'
gem 'uglifier',                       '~> 2.5'
gem 'jquery-rails',                   '~> 3.1'
gem 'compass-rails',                  '~> 2.0'

# Utils
gem 'pry',                            '~> 0.10', require: false
gem 'awesome_print',                  '~> 1.2',  require: false
gem 'log_buddy',                      '~> 0.7',  require: false
gem 'airbrake',                       '~> 4.0'
gem 'nifty_settings',                 '~> 1.1'
gem 'newrelic_rpm',                   '~> 3.9'
gem 'tries',                          '~> 0.3'
gem 'rack-mini-profiler',             '~> 0.9'
gem 'whenever',                       '~> 0.9', require: false
gem 'oj',                             '~> 2.9'
gem 'squeel',                         '~> 1.2'

# Services
gem 'services',                       '~> 0.1'

# Postgres
gem 'pg',                             '~> 0.17'
gem 'postgres_ext',                   @rails_major_version == 3 ? '~> 1.0' : '~> 2.3'
gem 'schema_plus',                    '~> 1.5'

group :development do
  gem 'bullet',                       '~> 4.12'
  gem 'letter_opener',                '~> 1.2'
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
