---
layout: post
title: Migrating to Github Pages
---

Recently, I transitioned my site from Heroku by Salesforce to Github Pages and I couldn't be more happy with the switch. Heroku is a great platform, but not the right tool for this site. I built it using Jekyll, which means I have no reason to be using a full web stack with Apache, MySQL, and PHP.

## Why I Switched

Github Pages is so much simpler than Heroku. I don't need all of the power that Heroku has for my simple portfolio site, and the simplicity of Hithub allows me to be much more productive.

Github Pages is fast. Really Fast. Acording to the [test I ran on Pingdom.com](http://tools.pingdom.com/fpt/bPwb6Q/http://www.ryanslama.com/), my site loads in 141 milliseconds and is faster than 99% of all websites. Github achieves this by using Fastly as their content download network. As the name implies, Fastly is lightning fast. Additionally, Github pages has great uptime. Significantly better uptime than if I were updating a server (or dyno) by myself.

## The Problems I Encountered

Static sites, like those built from Jekyll, cannot process a web form. I have a contact form on my site, but had no way of reading the data from a simple HTML site. I did some research and realized I had a few options.

1. I could use a 3rd party service to host my form
2. I could use FormKeep to manage my responses
3. I could use Brace Forms to recieve emails of any form inputs

The first thing I did was eliminate option #1. As a web developer, I hate relying on another service to host my code. Plus, a form looks so much better if it is a part of a website rather than a similarly styled website that is hosted elsewhere. 

Then, I decided to try Formkeep, and I really liked it. With 2 lines of code, it will capture all of your form responses and put them in an excellent web interface. Unfortunatly, Formkeep does not have a simple method of email or text notifications, so I was forced to look further. Note: Formkeep does support Webhooks, but I did not want to complicate my setup any more than it needed to be.

Finally, I have settled upon Brace Forms. Like Formkeep, it takes a very small amount of code and records all your responses. Unlike Formkeep, it does not have a web interface. Rather, it will email every form submission to you and it was the perfect solution for my contact form. 

Overall, I am very happy with my decision to move to Github pages and I would recommend it to anyone looking to host a simple, static site.