---
layout: post
title:      "Sinatra Web App Project"
date:       2020-01-26 15:07:11 +0000
permalink:  sinatra_web_app_project
---


My second project for the software engineering course was to make a web app using Sinatra and I was really excited about it. I decided that I wanted to try and make something that I could use to help make a simple task a little easier. So I decided to make a shipping app that tracks different retailers that get sent out at the end of the week. It is based around what I do at work so I thought it would be cool to come up with it and maybe even possibly use it at some point.

I started by planning out how I wanted to attack this project based on the project requirements that were given to me. I had to build an MVC Sinatra application. MVC stands for Models, Views and Controllers and they all work together to make your application come together along with the use of ActiveRecord which is an amazing tool that you can utilize. ActiveRecord is used to create tables then users can create, read, update and delete. Programmers use CRUD to help them build Sinatra apps cause you need build out your controllers you are using based on that.

Now that I knew what I was going to do i started with making my database using rake commands in my terminal. Rake is just a ruby gem that you can install through your terminal and use. I created two tables that I was going to use one for users and one for retailers. The next step is to add the columns to the tables for the users I added two cloumns, one for email and one for password. The retailers columns that were added were a name, boxes and user id. Now I have a way to make tables and add data to them. Once I have that accomplished I need to migrate my tables so I could use them. Rake has a command that I use for that db:migrate and it takes care of everything for you.
 
This is the models section of the program.

The next step was setting up my has many and belongs to realtionships which were a little tricky but I was able to get them sorted out. users has_many retailers, retailers belong_to users. The requirement for the project was to "Use at least one has_many relationship on a User model and one belongs_to relationship on another model.". Which I had set up so another requirement was met.

This is the controllers section of the program.

The next step was starting to work out my controllers and how to set up my routes. The controllers use RESTful routes which is basically a pattern that allows us to code where we want each action to go. There are a few different http verbs that they use to describe these different routes. The ones that I used were GET, POST, PATCH and DELETE.  I used the CRUD model again to set up my routes based on those actions. It gave me an easy way to identify exactly what each http request was doing and when I ran into errors later in the project I would knoe exactly what i was working with. I have three controllers that I used for this program an application, user and a retailer. Each one of those controllers play an important part in what I am trying to do with each page that the user is taken to. Once I have all the routes figured out then I move on the next step which is views.

This is the views section of the program.

Once I had the routes set I need a way to make them viewable to the user using the program that is where the views come in to play. I need to make a view page for the user to see all the retailers they have which I called the index page. The next view I need was for when the user created a new retailer and that was called the new page. Now that we created the new retailer we need a way to view it and that is the show page where it displays what was just created. Next is the edit page where a user can go and edit a retailer if they need to, I'm sure you know where I'm going with this, you would be correct if you said an edit page. Now that all those are created and coded I can start testing and dealing with any errors that may come up.

When I start checking to make things work I use the shotgun command in the terminal and it opens a local port that I can use in a web browser. All I do is go through all the pages and add the required data that is asked for to make sure it all flows together. If there is an issue Sinatra lets me know what the error is, where in the program it is and what line of code is causing it. 

I learned a lot during this project and it tested me at times but I know it will be all worth in the end.
