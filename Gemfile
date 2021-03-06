source 'https://rubygems.org'

group :active_record do
  platforms :jruby do
    case ENV['CI_DB_ADAPTER']
    when 'mysql'
      gem 'activerecord-jdbcmysql-adapter', '>= 1.2'
      gem 'jdbc-mysql', '>= 5.1'
    when 'postgresql'
      gem 'activerecord-jdbcpostgresql-adapter', '>= 1.2'
      gem 'jdbc-postgres', '>= 9.2'
    else
      gem 'activerecord-jdbcsqlite3-adapter', '>= 1.3.0.beta1'
      gem 'jdbc-sqlite3', '>= 3.7'
    end
  end

  platforms :ruby, :mswin, :mingw do
    case ENV['CI_DB_ADAPTER']
    when 'mysql2'
      gem 'mysql2', '~> 0.3.14'
    when 'postgresql'
      gem 'pg', '>= 0.14'
    else
      gem 'sqlite3', '>= 1.3'
    end
  end
end

group :mongoid do
  gem 'mongoid', github: 'mongoid/mongoid'
  gem 'mongoid-paperclip', '>= 0.0.8', require: 'mongoid_paperclip'
  gem 'mongoid-grid_fs', github: 'ahoward/mongoid-grid_fs'
  gem 'carrierwave-mongoid', '>= 0.6.3', require: 'carrierwave/mongoid'
end

group :development, :test do
  gem 'pry', '>= 0.9'
  gem 'pry-rescue', '>= 1.2'
  platforms :mri_19, :mri_20 do
    gem 'pry-debugger', '>= 0.2'
    gem 'pry-stack_explorer', '>= 0.4.9.1'
  end
end

group :test do
  gem 'cancan', '>= 1.6'
  gem 'capybara', '>= 2.1'
  gem 'carrierwave', '>= 0.8'
  gem 'coveralls', require: false
  gem 'database_cleaner', '>= 1.2'
  gem 'devise', '>= 3.2'
  gem 'dragonfly', '~> 1.0'
  gem 'factory_girl', '>= 4.2'
  gem 'generator_spec', '>= 0.8'
  gem 'launchy', '>= 2.2'
  gem 'mini_magick', '>= 3.4'
  gem 'paperclip', '3.5.2'
  gem 'poltergeist', '~> 1.5'
  gem 'rack-cache', require: 'rack/cache'
  gem 'rspec-rails', '>= 2.14'
  gem 'rubocop', '>= 0.15'
  gem 'simplecov', require: false
  gem 'timecop', '>= 0.5'
end

platforms :rbx do
  gem 'racc'
  gem 'rubinius-coverage'
  gem 'rubysl'
  gem 'rubysl-test-unit'
end

gemspec
