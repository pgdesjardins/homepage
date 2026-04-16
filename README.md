# Jekyll Homepage

Category index page. Data lives in `_data/hyperlinks.yml`.

## Ruby Setup

Uses Ruby 3.3.4 (matches GitHub Pages built-in builder).
System Ruby (2.6) will not work — install rbenv first.

```bash
brew install rbenv ruby-build
echo 'eval "$(rbenv init - zsh)"' >> ~/.zshrc
source ~/.zshrc

rbenv install 3.3.4
rbenv local 3.3.4   # writes .ruby-version
ruby -v             # should show 3.3.4
```

## Install & Run

```bash
gem install bundler         # installs latest bundler (4.x)
gem uninstall bundler -v 1.17.2 --force 2>/dev/null; true
bundle _4.0.10_ install     # force new bundler, avoids BUNDLED WITH 1.17.2 in lock
bundle exec jekyll serve
```

## Deploy

Push to a GitHub repo and enable Pages (Settings → Pages → Deploy from branch).  
No GitHub Actions needed — the built-in builder handles it.
