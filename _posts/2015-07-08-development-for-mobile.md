---
layout: post
title: Rails Custom Port and IP address
cover: leap.jpg
date:   2015-07-08 11:55:00
categories: posts
---

## To Start Off

I have to say, it is quite intimidating thinking about what topics to post about now. After finishing DBC, mind has been all about finding a job (obviously from my ~~last~~ only two posts) and giving myself validation for all the hard work I've completed. So much so this "blog" has essentially become more about me trying to motivate readers (mostly myself) to keep my head up. But people, I'm trying! Again, I feel like I'm taking a leap of faith, but this time in blogging and hopefully something that someone out there will find useful.

I can't guarantee I'll be 100% accurate, I can't guarentee what I write will be interesting to you, but I can guarantee it's 100% heart and will be whatever tidbit I've learned as I continue my journey as a web developer. So here goes...*holds breath*

## Development for Mobile

*Situation*
You're developing a Rails web application and of course the first thing you think of is "MOBILE FIRST." You begin your journey of responsive design and coding and find yourself unable to test what it would really look like on your phone. (Chrome has the handy dandy little *Inspect Element* {for those of you who are new to coding, you'll find that in Chrome browsers and just right-click anywhere on the page}, but it can be finicky sometimes.)

You really want to try the app you've just coded on your ACTUAL phone, so what is a developer to do?

**First** make sure you have WIFI access and that **both the computer and phone are connected to the same WIFI**.

Running a rails server:
`rails s`  or same as `rails serve`

*You'll notice that the* default IP is: localhost (*or same as* 127.0.0.1)
                    and default port is: 3000

To change your IP:

`rails s -b <your IP address>`

example:

`rails s -b 123.4.5.6`

Finding your IP address:

1. go to Terminal (I only know Mac, for now.. sorry)
2. type in: `ifconfig`
3. TADA it should be somewhere there
   a. check in the **en0** area and should be next to **inet**

To change your port (you don't need this step, but thought it would be a nice to know):

`rails s -p <new port number here>`

example:

`rails s -p 2000`

*you can also combine the two (yay!)*

example:

`rails s -p 2000 -b 127.0.0.1`

And **there you have it**! Now you can go to your phone's browser and just type in the URL bar:

`<IP address:port number>`

example:

`127.0.0.1:9898`

Hope this helps someone! Thanks for reading!

Peace.