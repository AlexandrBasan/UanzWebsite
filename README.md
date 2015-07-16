# UANZ project

    $ cd /tmp
    $ cd uanz
    $ cp config/database.yml.example config/database.yml
    $ bundle install
    $ bundle install --without production
    $ bundle exec rake db:migrate
    $ bundle exec rake db:test:prepare
    $ bundle exec rspec spec/

If the tests don't pass, it means there may be something wrong with your system. If they do pass, then you can debug your code by comparing it with the reference implementation.

Heroku

    $ rake assets:precompile
    $ RAILS_ENV=production bundle exec rake assets:precompile
    $ git push heroku master
    $ heroku rake db:migrate
    $ heroku restart
    $ heroku open
