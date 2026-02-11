# frozen_string_literal: true

source "https://rubygems.org"

gem "jekyll-theme-chirpy", "~> 7.3"

gem "html-proofer", "~> 5.0", group: :test

# 将 :mingw, :x64_mingw, :mswin 统一替换为 :windows
platforms :windows, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# 同样修改这里的 platforms
gem "wdm", "~> 0.2.0", :platforms => [:windows]

gem 'jekyll-compose', group: [:jekyll_plugins]
