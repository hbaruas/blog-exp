---
layout: post
title: Create a static website using Jekyll and how to host on Github pages.
summary: Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde, dolore.
---


In this post I will be creating, a static website using jekyll, please go through the following installation guide to install required things, for the sake of not making this post very long I am, not writing about how to install everything in detail.

#### INSTALLATION

1.	Install ruby for windows here is the link <a href="https://rubyinstaller.org/downloads/" target="_blank">https://rubyinstaller.org/downloads/</a> 
2.	While installing a popup will come in the end make sure you have selected that.
3.	In CMD install all the other dependencies  By pressing  1,2,3 and enter
4.  Check whether ruby has installed or not.
<br/>

##### Terminal
 {% highlight Bash %}
 ruby –v
 gem –v
 {% endhighlight %}
if these two commands are giving output as a version then it means it has installed.

5.Install Jekyll using gem, run command 
##### Terminal
{% highlight Bash %}
gem install jekyll bundler
{% endhighlight %}

6.Run  
##### Terminal
{% highlight Bash %}
Jekyll  -v
{% endhighlight %}
it must give an output telling that which version has been installed.
So far installation is complete.
#### Starting the new website.
Navigate to your desired folder where you want to create the directory structure for your newly created site and run the following command.
##### Terminal
{% highlight Bash %}
Jekyll new your_website_name
{% endhighlight %}

Output would be something just like this.
<img src="{{ "../img/Jekyllsite/jekyll-first-time.jpg" | relative_url }}" alt ="first time when" class="img-fluid"/>

Now the website the basic skeleton has been developed the only thing we need to do is to start the local server and test, we can start the server using the following command.
##### Terminal
{% highlight Bash %}
bundle exec jekyll serve 
{% endhighlight %}

it will start the server and will tell where we can check it
<img src="{{ "../img/Jekyllsite/jekyll-serve.jpg" | relative_url }}" alt ="jekyll-serve" class="img-fluid"/>

Now if we type the given url in our browser, we can see our recently created site, and the output will be something like this.

The folder structure of the newly created static site will look something like this.
<img src="{{ "../img/Jekyllsite/first-time-in-browser.jpg" | relative_url }}" alt ="folder structure" class="img-fluid"/>

you can click on by default created very first post Welcome to Jekyll! and it will lead to a page having very useful basic information that how we can create the post and what other things you can do with jekyll.

Now we need to have a look in the file and directoris created by jekyll by default, I am using Sublime Text text editor and that's how it looks like.
<img src="{{ "../img/Jekyllsite/folder-structure.jpg" | relative_url }}" alt ="folder structure" class="img-fluid"/>

very first directory is for cached data, next directory is for where we are going to put all our posts, here we can see a markdown file, this is the same content which is being shown while we clicked on the by default created post.

next directory is site this is the one where actually all of our compiled website is stored we don't need to touch this folder as everything is being auto compiled and generated here by jekyll itself.

we have a 404.html, a standard 404 page in case of some wrong URL is being passed.

config.yml file is where all the front matter and everything will be define.

then we have about.md page there this is the layout of already created about page.

we have two gemfiles there you can see all the installed gems and you can also see the default theme being used by jekyll called "minima".

Then we have index.md there is nothing much inside it just the layout is given just the name of layout is given here which is being provided by default theme "minima". We can define our own layout as well.

let's discuss few more things prior to create a new post.










