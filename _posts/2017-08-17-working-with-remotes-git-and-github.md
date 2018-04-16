---
layout: single
header:
  overlay_color: "#5e616c"
  overlay_image: /assets/img/stanford-hills-big.jpg
title:  "Working with remotes: Git and Github"
date:   2017-07-09 02:54:58 +0100
categories: tutorials git
excerpt: Git is a powerful version control utility that provides a wide vista of possibilities. Here I briefly explain a simple workflow for working with remotes on git.
---
This brief tutorial assumes at least a minimal knowledge of the version control tool called git. If you don't have that basic knowledge, not to worry. You can take this 15 minute crash course [Git Tutorial](https://try.github.io) or the [Codecademy git tutorial](https://www.codecademy.com/en/courses/learn-git)

I wrote this basically as a referrence to use when working on a remote with several collaborators. 

This tutorial will be making use of github as the host of the sample remotes

In order to work with any remote, you need to first get the location of the repository that you want to work on.

Step 1: then do a `git clone` viz:

{% highlight github %}
$ git clone https://github.com/your-remote-repository/repository-folder/
{% endhighlight %}

Step 2: Next you change directory into the particular `repository folder`
{% highlight github %}
$ cd repository-folder
{% endhighlight %}

You are now ready to make your own contribution to the project.

After making your file changes and making your named commits, it is very likely that other contributors to the same project would have also made changes and pushed these changes to the repository. Hence the next step:

Step 3: You need to fetch and merge whatever changes or commits have been made during the interim by doing a `git pull`

{% highlight github %}
$ git pull
{% endhighlight %}

This command gets the latest commits from the remotes origin/master and merges it to your local version of the repository.

Optional step: Now it is possible you get a message from the terminal thus: "Please enter a commit message to explain why this merge is necessary,especially if it merges an updated upstream into a topic branch"

To solve this:

press `i` on your keyboard
write your merge message
press `esc`
write ":wq"
then press `enter`

Last step: Finally, you can now push your commits to the remote repository:
{% highlight github %}
$ git push
{% endhighlight %}

You will be prompted as usual for your username and password. Supply these and proceed.

That about wraps it up.

To summarize, your work flow looks something like this:

{% highlight github %}
$ git clone https://github.com/your-remote-repository/repository-folder/
$ cd repository-folder
$ git pull
$ git push
{% endhighlight %}

