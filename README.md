# site setup

## Initial setup

```shell
chruby $(cat ~/.ruby-version)

cat > Gemfile <<EOF
source 'https://rubygems.org'

#gemspec
gem "github-pages", group: :jekyll_plugins
EOF
chmod 0644 Gemfile

gem install bundler jekyll
bundle install

```

## Maintaining https://ns408.github.io/

### Making changes

- modify `index.md` and view changes before pushing it to the repository.

### Testing your changes

```
gem install --no-rdoc --no-ri bundle
bundle install
bundle exec jekyll serve
```
