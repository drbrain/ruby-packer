$LOAD_PATH.unshift File.expand_path "lib"

require "compiler"

task default: :build

rubyc = "rubyc-#{Compiler::VERSION}-#{RUBY_PLATFORM}"

task build: rubyc

file rubyc do
  sh "ruby", "-I", "lib", "bin/rubyc", "bin/rubyc"
  mv "a.out", rubyc
end
