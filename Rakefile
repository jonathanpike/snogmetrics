require 'bundler'
require 'yard'
require 'spec/rake/spectask'

task default: :spec

Bundler::GemHelper.install_tasks

YARD::Rake::YardocTask.new

Spec::Rake::SpecTask.new(:spec) do |spec|
  spec.libs << 'lib' << 'spec'
  spec.spec_files = FileList['spec/**/*_spec.rb']
end

Spec::Rake::SpecTask.new(:rcov) do |spec|
  spec.libs << 'lib' << 'spec'
  spec.pattern = 'spec/**/*_spec.rb'
  spec.rcov = true
end
