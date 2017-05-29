# Ruby on Rails Notes

Ruby on Rails is a:
  - Web framework for developing web applications
  - A Ruby Gem (a set of Ruby code libraries).
  - A Model-View-Controller Framework, a.k.a. MVC.
    - Model: location for application's logic
    - Controllers: manage code flow
    - View: displays content to the user

## Commands

| Command | Use |
| --- | --- |
| `rails new NAME` | creates a new rails application
| `rake db:create` | create the database
| `rails s` | start the rails server

## The Rails Console
Allows you to:
- Run database queries
- Run application code
- Perform full CRUD tasks with the database
- Switch between making permanent database changes and running in a sandbox mode to test scripts out

Use `rails c` to open the console and `control + d` to close it.

| Command | Use |
| --- | --- |
| `helper.pluralize(#, 'word')` | takes in a word and returns the plural equivalent based off the given number amount

## Directory Structure/Files

| Directory | Description |
| --- | --- |
| `app/` | contains the full MVC structure and non Ruby files, such as: css files, javascripts, images, fonts, etc. Changes can be made without need to restart the rails server
| `bin/` | contains built-in Rails tasks
| `config/` | contains many of the settings for you application
| `db/` | contains the database and `seeds.rb` file
| `lib/tasks/` | contains custom rake tasks
| `log/` | contains log files for your application that is useful for debugging
| `public/` | contains publicly facing error pages and the `robots.txt` file
| `test/` or `spec/` for RSpec | contains your specs, factories, test helpers, and test configuration files
| `tmp/` | contains temporary files and is rarely accessed by developers
| `vendor/` | integrating client-side MVC frameworks, such as AngularJS

| File | Description |
| --- | --- |
| `Gemfile` | contains all the libraries that are utilized in the application. After any change to the Gemfile, you will need to run bundle. This will call in all of the code dependencies in the application
| `Gemfile.lock` | displays all of the dependencies that each of the Gems contain along with their associated versions
| `README.rdoc` | used to document the details of the application
