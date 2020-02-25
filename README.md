# ATTENTION

Until further notice this web site is in the inital stages of preparation and is not expected to work or have useful content at any gien time.


# SCOPE

This is a static site intended to preserve the newly developed technical documentation for the PHENIX software infrastructure.

# TECHNICAL

## Gems
Pay attention to the following dependencies (need to be installed and also included in the Gemfile in this folder):
```
gem "jekyll", "~> 4.0"
gem 'jekyll-mentions', '~> 1.5', '>= 1.5.1'
gem 'jekyll-sitemap', '~> 1.4'
gem 'jekyll-redirect-from', '~> 0.16.0'
```
...and a few others. The best source is likely https://rubygems.org/

## Serving static content without Jekyll server
Links will need to be converted:
```
wget --convert-links -r http://localhost:4000/web/
```
