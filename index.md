# The TaubenCam, a useless quarantine project.

## Introduction

I am a freelance developer, currently not working and confined to my apartment in Berlin. Under these circumstances a person needs a project.

Last year a pair of wood pigeons came and nested on our balcony, where they raised two very ugly babies. This year they are back, and of course the natural thing to do is to attempt to broadcast this miracle of new life into a suffering world.

## Stage 0, Proof of Concept

### Hardware Resources

Amazon are still delivering, but this project should be done with the minimum amount of resources and expense. The initial hardware needed for the project was:

- a Raspberry Pi 4B
- a wide-angle camera ([this one](https://www.amazon.de/gp/product/B01ER2SMHY/ref=ppx_yo_dt_b_asin_title_o09_s00?ie=UTF8&psc=1).
- a freezer box

The Pi goes inside the freezer box, the camera sticks out of the side, and it all goes onto an empty plant holder on the wall. I had luck in this initial stage because right now the pigeons are only in their nest in the mornings, and it has not rained for a week. Making a new housing and waterproofing will feature in later stages of this project, so hang on.

### Network Reources
The Pi is on my local network, and there is a cheap (EUR4/month) virtual server somewhere in the cloud which is the public face of this project.

##W Software Resources

Of course everything will be open source.

For this initial step I want everything to be as simple as possible, so we use [motion](https://motion-project.github.io/), a very simple to use webcam package for the Pi, which streams  [mjpeg over http](https://en.wikipedia.org/wiki/Motion_JPEG#M-JPEG_over_HTTP) to http clients. In order to get this out onto the internet, I have rented a very cheap virtual server which uses [nginx](https://www.nginx.com/) to proxy http requests to the balcony Pi, and [nebula](https://github.com/slackhq/nebula), a very cool VPN from Slack to connect the two.

### Results

Pretty good, actually. The motion jpeg stream works well on most devices, the birds are charming, and don't seem phased at all by the presence of the camera. At this stage (mid-March) they are around until about 9am, so Peter (my husband) and I watch them on our phones from bed, and plot improvements. Here are some pictures of pigeons which I made
