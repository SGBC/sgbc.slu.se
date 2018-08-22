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

## Deploy to production

```shell
bundle exec jekyll build
git add _site
git commit -m "website update"
git subtree push --prefix _site origin web
```

*on the webserver:*

```shell
cd ~/github/sgbc.slu.se
git checkout web && git pull
mv web/* /var/www/default/
sudo chown -R root:apache /var/www/default/
sudo chcon -R --reference=/var/www /var/www/default/
```
