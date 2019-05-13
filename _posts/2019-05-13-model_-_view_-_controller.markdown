---
layout: post
title:      "MODEL - VIEW - CONTROLLER"
date:       2019-05-13 05:02:55 +0000
permalink:  model_-_view_-_controller
---


Completing my second project at Flatiron, building a MVC Sinatra App using ActiveRecord, was significantly less frustrating and at least as rewarding as the first project. The architectural pattern known as MVC separates an app into 3 main parts: model, view, & controller. 

* Model: The logic or brains of the app. This is where data is saved and manipulated. Generally, these are ruby classes of objects that will connect to a database to persist that data.
* View: The presentation... This is the 'front end', what the user will see. These are written in .erb files, primarily consisting of HTML and Ruby code.
* Controller: The courier between model and view. The controller is responsible for relaying data between the browser and the app. The controller will 'GET this data', run code on the data by using models, and then 'POST that data' by rendering the view (.erb) to the user.

In order to keep files organized while using this architectural pattern, we implement a concept called separation of concerns and single responsibility. Each file has a different responsibility. In doing this, we are more easily able to debug, troubleshoot, update, and maintain our code. Below is an example of a Sinatra MVC File Structure. 

├── Gemfile
├── README.md
├── app
│   ├── controllers
│   │   └── application_controller.rb
│   ├── models
│   │   └── model.rb
│   └── views
│       └── index.erb
├── config
│   └── environment.rb
├── config.ru
├── public
│   └── stylesheets
└── spec
    ├── controllers
    ├── features
    ├── models
    └── spec_helper.rb
		
When setting up these files, you will need to include your source url and required gems in Gemfile and run 'bundle' so that you are able to run all of your code. My Gemfile for this project looks like:

source "https://rubygems.org"

git_source(:github) {|repo_name| "https://github.com/#{repo_name}" }

gem 'sinatra'
gem 'sqlite3'
gem 'activerecord', :require => "active_record"
gem 'rake'
gem 'pry'
gem 'sinatra-activerecord'
gem 'shotgun'
gem 'bcrypt', '~> 3.1.7'
gem 'require_all'

You should also remember that you ApplicationController class in application_controller.rb will need to inherit from Sinatra::Base, while your Model class in model.rb will inherit from ActiveRecord::Base. 

Some of this is still pretty mystifying and magical in how it works. I'm excited to continue learning more and cannot believe how much progress I have made. Thanks for the read. 





