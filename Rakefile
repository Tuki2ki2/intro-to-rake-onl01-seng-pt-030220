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
  task :seed do
    require_relative './db/seeds.rb'
end

# namespace :db do
