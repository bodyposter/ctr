# Add your own tasks in files placed in lib/tasks ending in .rake,
# for example lib/tasks/capistrano.rake, and they will automatically be available to Rake.

require_relative 'config/application'

Rails.application.load_tasks

task :default => 'test_sqlite3'

%w(sqlite3).each do |adapter|
  namespace :test do
    task(adapter => ["#{adapter}:env", "spec"])
end
end