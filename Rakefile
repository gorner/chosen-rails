#!/usr/bin/env rake
require 'bundler/gem_tasks'
require File.expand_path('../lib/chosen-rails/source_file', __FILE__)

desc "Update with Harvest's Chosen Library"
task 'update-chosen', 'remote', 'branch' do |task, args|
  remote = args['remote'] || 'https://github.com/gorner/chosen'
  branch = args['branch'] || 'j-ui-kit-new'
  files = SourceFile.new
  files.fetch remote, branch
  files.cleanup
end
