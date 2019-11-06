---
layout: post
title:      "CLI Date Gem Project "
date:       2019-11-05 20:40:41 -0500
permalink:  cli_date_gem_project
---


My first project was to create a CLI Data Gem. I knew it was going to be a challenging but didn't realize how hard it was going to be. I knew I had all the tools to complete this project and it was just a matter of how to put it all together.

For my gem I decided to scrape a website and to gather my information that way. But as I started working though it, I came to realize quickly that it was going to be to difficult to do. So I did a complete 360 and changed what I was going to do. In hindsight I probably should have done more planning then i orginally did in the whole process. I guess you eventually learn how to plan for things both in coding and in real life.

I decided to use an API to do my project with. The one I chose to use was Open Brewery DB. I decided that I was going to use four different search parameters to pull information from the API for my user to get info about. The four parameters I chose were the breweries name, address, city and state where it can be found. The next step was to figure out how to put what I wanted to do into actual code.  I sat down and thought about what i wanted to do. I said out loud what I wanted to accomplish and proceeded to type it out into my text editor. I ran into some snags while working it out but I was able to pop open a new window in my browser and search google to help me to understand what I needed to do. I broke my project down into three different sections. 


My API class is where I built a method that I could access the API from. I am able to pull the data I wanted to get from here. I used open uri to access the API and then I used JSON to parse the data that I collected from it so it was in a readable format. The code below is what I used.  I also put a hash of all the states that are available to search through. I needed to make sure that I had a valid state from the user input and that it was free of spelling errors. If any of those two variables weren't correct then I need a way to let the user know they had to fix it. I actually made a method in the CLI class that would do just for me. Now I am able to ask for input but also have a way to make sure everything is good.

``` def self.get_breweries(state)
    data = open("https://api.openbrewerydb.org/breweries?by_state=#{state}").read
    JSON.parse(data)
  end

```

I was then able to write a CLI class where I put all the functionality of the program at. It is there so the person has a visable menu with prompts that help direct them as they move through it. I made sure that I had good instructions for them to follow so they wouldn't get confused as they use it. 

I have learned a lot as I went though this module and through this project. I know that this is only the start but I am looking forward to continuing along this program.





