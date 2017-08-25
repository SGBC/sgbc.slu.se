## Deploy

*TODO*

## Get a local development version

for deploying a development version of the site

```shell
gem install bundler
bundle install
bundle exec jekyll serve
```

if you are working on a mac and have a brewed version of libxml2, add this
step before `bundle install`

```
bundle config build.nokogiri --use-system-libraries \
  --with-xml2-include=$(brew --prefix libxml2)/include/libxml2
 ```
