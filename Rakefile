desc 'outputs hello to the terminal'
task :hello do
  puts "hello from Rake!"
end

task :environment do
  require_relative './config/environment'
end


namespace :db do
  desc 'migrate changes to your databse'
  task :migrate => :environment do
    Student.create_table
  end
end

namespace :db do
  task :seed do
    require_relative './db/seeds.rb'
  end
end

namespace :db do
  task :console =>:environment do
    Pry.start
  end
end
