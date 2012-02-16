# encoding: utf-8

require 'rubygems'
require 'rake'

require 'jeweler'
Jeweler::Tasks.new do |gem|
  # gem is a Gem::Specification... see http://docs.rubygems.org/read/chapter/20 for more options
  gem.version = "1.14.10"
  gem.name = "guestfs"
  gem.homepage = "http://github.com/rubiojr/guestfs"
  gem.license = "MIT"
  gem.summary = "Ruby bindings for libguestfs"
  gem.description = "Ruby bindings for libguestfs"
  gem.homepage = "http://libguestfs.org/"
  gem.email = "rjones@redhat.com"
  gem.authors = ["Richard WM Jones"]
  gem.required_ruby_version = '>= 1.8.1'
  # dependencies defined in Gemfile
end
Jeweler::RubygemsDotOrgTasks.new

require 'rake/testtask'
Rake::TestTask.new(:test) do |test|
  test.libs << 'lib' << 'test'
  test.pattern = 'test/**/test_*.rb'
  test.verbose = true
end

task :default => :test

require 'rake/rdoctask'
Rake::RDocTask.new do |rdoc|
  version = File.exist?('VERSION') ? File.read('VERSION') : ""

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "guestfs #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end
