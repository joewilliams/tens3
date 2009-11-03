require 'rubygems'
require 'rake/gempackagetask'
require 'rake/rdoctask'

spec = Gem::Specification.new do |s|
  s.name = "tens3"
  s.version = "0.1"
  s.author = "joe williams"
  s.email = "joe@joetify.com"
  s.homepage = "http://github.com/joewilliams/tens3"
  s.platform = Gem::Platform::RUBY
  s.summary = "easy backups to s3"
  s.files = FileList["{bin}/**/*"].to_a
  s.has_rdoc = true
  s.extra_rdoc_files = ["README"]
  %w{fadvise right_aws}.each { |gem| s.add_dependency gem }
  s.bindir = "bin"
  s.executables = %w( tens3_put tens3_get)
end

Rake::GemPackageTask.new(spec) do |pkg|
  pkg.need_tar = true
end

Rake::RDocTask.new do |rd|
  rd.rdoc_files.include("bin/*")
end
