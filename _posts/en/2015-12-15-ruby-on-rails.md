---
layout: post
published: true
exacttime: "16:00:00"
title: "Starting off with Ruby or Rails"
category: "Ruby"
headimg_url: "/images/rails/rails.jpeg"
headimg_lic: "By MichaelMaggs (Own work) [CC BY-SA 3.0], via Wikimedia Commons"
headimg_lic_url: "http://commons.wikimedia.org/wiki/File%3ACello_study.jpg"
---
###### Navigating through rails:

app folder - Where we do most of our work 
Controllers are where the different options for each post are located.

Views are where we implement what the pages will look like.

config -> root.rb -> root to out controller and view

changed the view.htmlerb file and get the new page.
Yay !!
^^Check steps above^^

irb is the command you will use to get ruby running 

Basically a fancy editor 
No need of compilation of ruby 
It is probably interpreted line by line 
Ruby is cross platform 
Always try to make functions cross-platform as there are some differences in the syntax for win or for mac 
Thus make sure you consider cross-platform dependencies Rails is just a framework 
Ruby is Object Oriented 
10th most popular language 
can use heroku or github to host stuff
Heroic may turn out to be expensive 
GitHub is best 
Jekyll is nice 
Ruby packages are a pain in the ass 

rails generate controller name
rails console 
 |
 |
 |
 |
 V
Inside the console 
FUNCTIONS FOR POSTGRES DATABASE ELEMENTS

new
save -> create is one way short-cut

table.attribute = whatever
table.save
table.update_attribute(VAR, NEW VALUE )
table.update_attributes(    )
ALWAYS HAVE A : BEFORE A TABLE VAR AND A @ BEFORE A VAR IN HTML THAT USES RUBY !!

Embedding Ruby in HTML isn’t pretty, but then again so isn’t PHP 

<%= FOR SHOWING STUFF ON THE SCREEN %>
<% FOR NOT SHOWING STUFF %>

 @post = Post.find(params[:id])

strftime() is kind of useful
%b %d. %Y
link_to post.title, post
form_for 
stylesheet_link_tag
javascript_include_tag
flash messages are run using key value pairs 
^^They are important for us to 

AWS is used to put stuff on the net before heroku can actually find it 
Don’t use filezilla if you don’t have your own site yet(hopefully soon ;))

So next up something called scaffolding(from prior experience this is not going to be pretty)
Kind of useful

Active Admin is hard to use on newer versions of ruby 
It doesn’t work well

seed along with migrate

“/….” match :to => “/::::::”
