# frozen_string_literal: true

source "https://rubygems.org"

gemspec

gem "debug", platform: :mri

eval_gemfile "gemfiles/rubocop.gemfile"

local_gemfile = ENV.fetch("LOCAL_GEMFILE", "Gemfile.local")

if File.exist?(local_gemfile)
  eval(File.read(local_gemfile)) # rubocop:disable Security/Eval
else
  gem "activerecord", "~> 7.0"
end
