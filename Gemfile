source "https://rubygems.org"

# Ruby 3.4+ removed these from the default gems.
gem "csv"
gem "bigdecimal"

# --- Local preview only ---
# This site normally targets the "github-pages" meta-gem so local builds
# match GitHub Pages' production environment exactly. That gem hard-pins
# very old liquid/kramdown/commonmarker versions, none of which work on
# modern Ruby (e.g. Ruby 4.0 -- either an unsolvable dependency conflict,
# or a runtime crash from calling String#tainted?, which Ruby removed in
# 3.2+). GitHub Pages builds the live site on its own servers and never
# reads this Gemfile, so swapping to plain modern Jekyll here for local
# `jekyll serve` has zero effect on the deployed site.
gem "jekyll", "~> 4.3"
gem "kramdown-parser-gfm"
gem "rouge"

group :jekyll_plugins do
  gem "jekyll-feed"
  gem "jekyll-sitemap"
  gem "jekyll-paginate"
  gem "jekyll-redirect-from"
  gem "jekyll-gist"
end

gem "wdm", "~> 0.1.0" if Gem.win_platform?

# Resolve an error on windows
# => jekyll 3.9.0 | Error:  No source of timezone data could be found.
gem 'tzinfo-data', platforms: [:mingw, :mswin, :x64_mingw]
