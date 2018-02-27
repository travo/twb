#!/usr/bin/env rake
require 'pry'
require 'erb'
require 'active_support/inflector'
require 'fileutils'

I18n.enforce_available_locales = false

desc 'Publish traviswintersband.com'
task publish: :build do
  sh 'rsync -avz www/_out/* traviswintersband.com:~/www/documents/'
end

desc 'Build the website using Pith.'
task :build do
  sh 'pith -i www build'
end

desc 'Build the website using Pith.'
task :serve do
  sh 'pith -i www serve'
end
