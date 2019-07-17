---
layout: post
title: Create a static website using Jekyll and how to host on Github pages.
summary: In this post, I will be writing about how to start a static jekyll site and host it for free using github page.
---


In this post I will be creating, a static website using jekyll, please go through the following installation guide to install required things, for the sake of not making this post very long, I am not writing about how to install everything in detail.

And that's how our end project will look like

<img src="{{ "/img/Jekyllsite/Final_product.JPG" | relative_url }}" alt ="Final product" class="img-fluid"/>

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
<img src="{{ "/img/Jekyllsite/jekyll-first-time.JPG" | relative_url }}" alt ="first time when" class="img-fluid"/>

Now the website the basic skeleton has been developed the only thing we need to do is to start the local server and test, we can start the server using the following command.
##### Terminal
{% highlight Bash %}
bundle exec jekyll serve 
{% endhighlight %}

it will start the server and will tell where we can check it
<img src="{{ "/img/Jekyllsite/jekyll-serve.JPG" | relative_url }}" alt ="jekyll-serve" class="img-fluid"/>

Now if we type the given url in our browser, we can see our recently created site, and the output will be something like this.

The folder structure of the newly created static site will look something like this.

<img src="{{ "/img/Jekyllsite/first-time-in-browser.JPG" | relative_url }}" alt ="folder structure" class="img-fluid"/>

you can click on by default created very first post Welcome to Jekyll! and it will lead to a page having very useful basic information that how we can create the post and what other things you can do with jekyll.

Now we need to have a look in the file and directoris created by jekyll by default, I am using Sublime Text text editor and that's how it looks like.

<img src= "{{ "/img/Jekyllsite/folder-structure.JPG" | relative_url }}" alt ="folder structure" class="img-fluid"/>

very first directory is for cached data, next directory is for where we are going to put all our posts, here we can see a markdown file, this is the same content which is being shown while we clicked on the by default created post.

next directory is site this is the one where actually all of our compiled website is stored we don't need to touch this folder as everything is being auto compiled and generated here by jekyll itself.

we have a 404.html, a standard 404 page in case of some wrong URL is being passed.

config.yml file is where all the front matter and everything will be define.

then we have about.md page there this is the layout of already created about page.

we have two gemfiles there you can see all the installed gems and you can also see the default theme being used by jekyll called "minima".

Then we have index.md there is nothing much inside it just the layout is given just the name of layout is given here which is being provided by default theme "minima". We can define our own layout as well.

let's discuss few more things prior to create a new post.

The name format of the post should be exactly similar to the one given post under posts folder, i.e. first date in the same format, and then post name if there is a space in the name of the post, that will be replace by the hyphen.

<img src="{{ "/img/Jekyllsite/post_name.JPG" | relative_url }}" alt ="post name sample" class="img-fluid"/>

Now create a new file as per the rules mentioned above, somwthing like this.

<img src="{{ "/img/Jekyllsite/first_sample_post.JPG" | relative_url }}" alt ="first sample post" class="img-fluid"/>

now paste this content in your newly created file.

##### code for new post
{% highlight HTML %}
---
layout: post
title:  "posted very first time"
---
Hi this post is being created very firstt time, hopefully it should work
{% endhighlight %}

save it and refresh your page, output will be something just like this.

<img src="{{ "/img/Jekyllsite/new_post.JPG" | relative_url }}" alt ="new sample post" class="img-fluid"/>
if you will click on this the new page will open and you can see your detailed post.

<img src="{{ "/img/Jekyllsite/detail_post.JPG" | relative_url }}" alt ="first detailed post" class="img-fluid"/>

Now we know how to create a new blog post let's dig a bit deeper and change few things.

Our goal is to change the highlighted things in below image.

<img src="{{ "/img/Jekyllsite/things_to_update.JPG" | relative_url }}" alt ="this things we will update" class="img-fluid"/>

We can make all these changes by making change in config.yml file, one thing to note here, after making any changes in Config file we have to restart the server then only we can see the changes made by ourselves.

these are the changes we are going to make 
##### code for the config
{% highlight HTML %}

title: MY Blog #this is the new title 
email: abc@abc.com #this is the new email
description: >- # here you can define the description for your website
  this is the new description, this description will also be used by search 
  engines to show in the search result. 
baseurl: "" # the subpath of your site, e.g. /blog
url: "" # the base hostname & protocol for your site, e.g. http://example.com
twitter_username: saurabh_kumar # here you can provide your twitter user name
github_username:  hbaruas #here you can provide your github user name

# Build settings
markdown: kramdown
theme: minima
plugins:
  - jekyll-feed

{% endhighlight %}
Now close the server and restart it again, using the command Jekyll serve,
and hopefully everything should start looking something just like this.

<img src="{{ "/img/Jekyllsite/change_in_config.JPG" | relative_url }}" alt ="change in config file" class="img-fluid"/>

similar way you can make change in about.md file, you can add new content according to your need or modify the existing one, and if you think you need a new page you can create one similar to about.md make sure to change the name and change the permalink present in the front matter.
here I am creating a new page called as myself.md

##### code for the myself
{% highlight HTML %}
---
layout: page
title: Myself
permalink: /myself/
---
<h1>this is a sample post created for demo prupose.</h1>
<h1>this is a sample post created for demo prupose.</h1>
<h1>this is a sample post created for demo prupose.</h1>
<h1>this is a sample post created for demo prupose.</h1>
<h1>this is a sample post created for demo prupose.</h1>

{% endhighlight %}
and that's how the link will look like it will look,
<img src="{{ "/img/Jekyllsite/myself.JPG" | relative_url }}" alt ="myself position" class="img-fluid"/>

And that's how Myself page will look like.
<img src="{{ "/img/Jekyllsite/Myself_detail.JPG" | relative_url }}" alt ="myself detailed look" class="img-fluid"/>

that's pretty much it, your awesome blog is ready, you can host it anywhere, but we will be using github pages for that.

But this not the only thing you can do with jekyll, you can customize pretty much everything, even the website on you are reading this article is entirely designed using jekyll and being hosted on github pages.



















