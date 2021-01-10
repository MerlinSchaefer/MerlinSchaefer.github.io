---
layout: post
title:  "Enhancing my Spotify Experience with Python"
date: 2021-01-10 11:01:01 +0200
categories: Projects
---

# Enhancing my Spotify Experience with Python

[The best way to get a quick overview of the project is this Write Up](https://drive.google.com/file/d/1g80mcpEI1of5cVGCjPPZeU8SPDMndy1D/view?usp=sharing)

This [repository](https://github.com/MerlinSchaefer/spotify_app) contains the notebooks and scripts from the project.

## The Motivation
As an avid Spotify user and data enthusiast it was only a matter of time before I had to combine the two areas. I decided to explore the Spotify API with two main goals that would solve existing problems deriving from Spotify’s recommendations. 

## DUO.py
The first part of the project was the creation of a better Duos Playlist for my girlfriend and me by using our data obtained through the Spotify API.
We were not satisfied with the "Duo Mix" Playlist Spotify provided through our Spotify Duo Subscription. The artists seemed to be "correct" but the songs were not. 
It hardly offered any songs we actually both listened to and felt more like a wild guessing game based on our tastes than an actual combination of shared favorites and good recommendations.
Which is why I created a python script that creates a playlist that does just that: enter DUO.py
So far we are satiesfied with the results, and any ideas for improvement (such as leveraging machine learning) will be implemented soon.

## PlaylistBuddy
The spotify recommendations below each playlist are a nice feature, but depending on the playlist they sometimes feel a little unrefined.
I therefore took the liberty to try to refine them. The PlaylistBuddy will add 1-20 new songs to your playlist, based on Spotify's recommendations and either their similarity to the existing songs in a given playlist, their similarity to the "average" song of a playlist, some manually selected feature filters or all of the above.

## Further Resources

This [Medium Post](https://towardsdatascience.com/using-python-to-refine-your-spotify-recommendations-6dc08bcf408e) discusses some of the basic steps in the creation of PlaylistBuddy