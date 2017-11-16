require 'rake/testtask'

task default: %w[test]

task :run do
  ruby "./bin/othello"
end

task :win do
  ruby "./lib/window.rb"
end

multitask :gui => [:win, :run] do
end

Rake::TestTask.new do |t|
  ruby "./tests/helper.rb"
  t.libs << "test"
  t.test_files = FileList['tests/test*.rb']
  t.verbose = true
end
