desc 'outputs hello to the terminal'
task :hello do
  puts "hello from Rake!"
end

desc 'Loads environment'
task :environment do
  require_relative './config/environment'
end

desc 'Opens up pry console'
task :console => :environment do
  Pry.start
end

namespace :db do
  desc 'migrate changes to your database'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'Seeds the database tables with entries'
  task :seed do
    require_relative './db/seeds.rb'
  end
end

namespace :greeting do
  task :hello do
    puts 'hello from Rake!'
  end
  task :hola do
    puts 'hola de Rake!'
  end
end