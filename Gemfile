source 'https://rubygems.org'

# Specify Ruby version for compatibility
ruby '~> 3.0.0'

group :jekyll_plugins do
    require 'rbconfig'
    gem 'wdm', '>= 0.1.0' if RbConfig::CONFIG['target_os'] =~ /mswin|mingw/i
    gem 'jekyll', '~> 4.4.0'
    gem 'jekyll-archives', '~> 2.3.0'
    gem 'jekyll-diagrams', '~> 0.10.0'
    gem 'jekyll-email-protect', '~> 1.1.0'
    gem 'jekyll-feed', '~> 0.17.0'
    gem 'jekyll-imagemagick', '~> 1.4.0'
    gem 'jekyll-minifier', '~> 0.1.10'
    gem 'jekyll-paginate-v2', '~> 3.0.0'
    gem 'jekyll-scholar', '~> 7.2.0'
    gem 'jekyll-sitemap', '~> 1.4.0'
    gem 'jekyll-target-blank', '~> 2.0.2'
    gem 'jekyll-twitter-plugin', '~> 2.1.0'
    gem 'jemoji', '~> 0.13.0'
    # gem 'mini_racer'
    gem 'unicode_utils', '~> 1.4.0'
    gem 'webrick', '~> 1.9.1'
    # Pin open-uri to avoid uri gem conflict
    gem 'open-uri', '0.4.0'
end

group :other_plugins do
    gem 'httparty', '~> 0.23.1'
    gem 'feedjira', '~> 3.2.5'
end
