source 'https://rubygems.org'

gem 'rake'

platforms :ruby do
  gem 'sqlite3'
end

platforms :jruby do
  gem 'activerecord-jdbcsqlite3-adapter'
  gem 'jruby-openssl'
  gem 'mime-types', ['~> 2.6', '< 2.99']
end

platforms :rbx do
  gem 'psych'
end

group :test do
  if ENV['RAILS_VERSION'] == 'edge'
    gem 'actionmailer', :github => 'rails/rails'
    gem 'activerecord', :github => 'rails/rails'
  else
    gem 'actionmailer', (ENV['RAILS_VERSION'] || ['>= 3.0', '< 5.1'])
    gem 'activerecord', (ENV['RAILS_VERSION'] || ['>= 3.0', '< 5.1'])
  end

  gem 'coveralls', :require => false
  gem 'rspec', '>= 3'
  gem 'rubocop', '>= 0.25'
  gem 'simplecov', '>= 0.9'
end

gemspec
