require 'rspec/core/rake_task'
require 'bundler/gem_tasks'
require 'rubocop/rake_task'

# Default directory to look in is `/specs`
RSpec::Core::RakeTask.new(:spec)

task default: :spec

desc 'Run RuboCop on the lib directory'
RuboCop::RakeTask.new(:rubocop) do |task|
  task.patterns = ['lib/bread/**/*.rb']
  # only show the files with failures
  task.formatters = ['files']
  # don't abort rake on failure
  task.fail_on_error = false
end
