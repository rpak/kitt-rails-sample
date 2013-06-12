# Kitt Rails Sample

...

Generated with [Raygun](https://github.com/carbonfive/raygun).

# Requirements

To run the specs or fire up the server, be sure you have these:

* Ruby 1.9.3-p125
* PostgreSQL 9.x with superuser 'postgres' with no password (```createuser -s postgres```)
* PhantomJS for JavaScript testing (```brew install phantomjs```)

# Development

### First Time Setup

After cloning, run these commands to install missing gems and prepare the database.

    $ gem install bundler
    $ bundle update
    $ rake db:setup db:sample_data

Note, ```rake db:sample_data``` loads a small set of data for development. Check out ```db/sample_data.rb``` for details.

### Running the Specs

To run all ruby and jasmine specs.

    $ rake

Again, with coverage for the ruby specs:

    $ rake spec:coverage

### Running the Application Locally

    $ foreman start
    $ open http://0.0.0.0:3000

### Using Guard

Guard is configured to run ruby and jasmine specs, and also listen for livereload connections. Growl is used for notifications.

    $ bundle exec guard

### Deploying to Heroku

Install the heroku toolbelt if you don't already have it (https://toolbelt.heroku.com/).

    $ heroku apps:create kitt-rails-sample
    $ git push heroku master
    $ heroku run rake db:setup

# Considerations

...
