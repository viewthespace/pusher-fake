require "bundler/setup"
require "cucumber/rake/task"
require "rspec/core/rake_task"
require "yard"

Bundler::GemHelper.install_tasks

Cucumber::Rake::Task.new do |t|
  t.cucumber_opts = %w{--format progress --strict}
end

RSpec::Core::RakeTask.new do |t|
  t.pattern = "spec/**/*_spec.rb"
end

YARD::Rake::YardocTask.new do |t|
  t.files   = ["lib/**/*.rb"]
  t.options = ["--no-private"]
end

task default: [:spec, :cucumber]
