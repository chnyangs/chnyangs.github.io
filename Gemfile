# Local preview only. Classic GitHub Pages builds the site server-side and
# IGNORES this Gemfile, so nothing here affects the deployed site.
#
# Lean Jekyll 4 setup: avoids the github-pages gem's heavy dependency tree
# (activesupport 8 -> bigdecimal native build). For this simple site — kramdown,
# jekyll-sitemap, a custom layout — Jekyll 4 renders identically to Pages' Jekyll.
#
# First-time setup on Debian/Ubuntu system Ruby needs dev headers to build the
# native gems (eventmachine, ffi):
#   sudo apt-get install -y ruby-dev build-essential
#   bundle install
#   bundle exec jekyll serve   # -> http://127.0.0.1:4000
source "https://rubygems.org"

gem "jekyll", "~> 4.3"
gem "jekyll-sitemap"   # used in _config.yml
gem "webrick"          # required to run `jekyll serve` on Ruby 3.x
