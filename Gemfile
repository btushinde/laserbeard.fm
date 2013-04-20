source 'https://rubygems.org'
ruby '1.9.3'

def darwin_only(require_as)
  RUBY_PLATFORM.include?('darwin') && require_as
end

def linux_only(require_as)
  RUBY_PLATFORM.include?('linux') && require_as
end

gem 'rails', '3.2.13'
gem 'strong_parameters'
gem 'foreman'

# Server
gem 'unicorn'

#Database
gem 'pg'
# gem 'activerecord-postgres-hstore'

# Templating
gem 'slim'
gem 'slim-rails', :group => :development

# Form helpers
gem 'simple_form'

# Pagination
gem 'kaminari'
gem 'kaminari-bootstrap'

# Date and time
gem 'chronic'

# Settings (password)
# gem 'settingslogic'

# Queues
# gem 'queue_classic'

group :development do
  gem 'letter_opener'
  gem 'quiet_assets'
  gem 'better_errors'
  gem 'binding_of_caller'
  gem 'meta_request'
  gem 'pry-rails'
  gem 'pry-debugger'
  gem 'rails-erd' #generates ERD model diagrams 
end


group :assets do
  gem 'sass-rails'
  gem 'coffee-rails'
  gem 'uglifier', '>= 1.0.3'
  gem 'modernizr'

  # Bootstrap CSS
  gem 'bootstrap-sass'
  gem 'font-awesome-sass-rails'
end

gem 'jquery-rails'

group :development, :test do
  gem 'minitest-rails'
  gem 'factory_girl_rails'
  gem 'rb-fsevent', require: darwin_only('rb-fsevent')
  gem 'growl',      require: darwin_only('growl')
  gem 'rb-inotify', require: linux_only('rb-inotify')
  gem 'turn'
  gem 'spinach-rails'
  gem 'guard-minitest'
  gem 'guard-spinach'
end

group :test do
  gem 'minitest-rails-capybara'
  gem 'database_cleaner'
  gem 'simplecov', require: false
end

gem 'capistrano'
