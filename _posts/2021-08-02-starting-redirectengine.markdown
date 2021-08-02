---
layout: post
title:  "0: Getting Started: The idea, selecting the tech stack, and starting code"
date:   2021-08-02 13:24:26 -0400
# categories: jekyll update
---

<style>
.preview {
  height:100px;
  width:100px;
  display: inline-block;
  margin:2px;
}

.preview > div {
  display:flex;
  align-items: center;
  text-align: center;
  justify-content: center;
  height:100%;
}
</style>

# The Idea
I was peeved with trying to build redirects from my domains to other websites that could not be resolved with CNAMES. The exact issue that triggered this project's creation was when I wanted to make it easier for my teammates to access a team handbook hosted on OneDrive. I did not want to send them a long url, partially because I know it will be buried, and partially because I wanted the ability to easily share the url with someone orally. 

Unfortunately, OneDrive does not support custom domains (there really is no reason to) and I wanted a branded URL without having to use bit.ly or the like (bit.ly is firewalled at our location, so I wanted something more stable.)

# The Branding
After some research on domains, I settled on RedirectEngine as the name for this app, and after poking around coolors.co for a little while, I discovered a few colors I really like:

<div class="preview" style="background:#001B2E;color:white"><div>#001B2E</div></div>
<div class="preview" style="background:#294C60;color:white"><div>#294C60</div></div>
<div class="preview" style="background:#ADB6C4;color:white"><div>#ADB6C4</div></div>
<div class="preview" style="background:#FFEFD3;color:black"><div>#FFEFD3</div></div>
<div class="preview" style="background:#FE5F00;color:white"><div>#FE5F00</div></div>

I am not yet sold on most of them, so the color pallete is very much subject to change.


# The Tech Stack
As a JavaScript developer, I obviously wanted to stick with JS. I decided on using express.js mostly because of its simplicity. 

For oauth and other library support, I was stuck with the decision of Supabase or Firebase. I opted with Supabase because I had used it in previous projets and was more comfortable with it, and I personally have had some bad experiences working with Google Cloud Platform, so I am tentative about building my business on it.

For the database, I know that I will need at least 2 tables: users and redirect locations. For this project, I want to make an effort to protect the privacy of my users and collect as little information as possible, so I am going to collect as little information as possible (also helps to keep the database sizes low)

I am a big fan of DigitalOcean, so I will be hosting RedirectEngine on their App Platform paas service.

---

<iframe class="mj-w-res-iframe" frameborder="0" scrolling="no" marginheight="0" marginwidth="0" src="https://app.mailjet.com/widget/iframe/6gNQ/K5e" width="100%"></iframe>

<script type="text/javascript" src="https://app.mailjet.com/statics/js/iframeResizer.min.js"></script>