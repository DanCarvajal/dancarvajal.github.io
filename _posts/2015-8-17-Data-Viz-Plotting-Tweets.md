---
layout: post
title: Plotting My Tweets
---
Recently I begun to be interested in knowing more about my social media usage. I've been using some form of social media for over a decade now and I wanted see just how exactly I use it. My first thoughts were to Twitter because it's the platform I'm most active on and represented the largest source of data.

The first question I wanted to answer is *"How often do I tweet?"* Turns out this question is one of the easier ones to answer. Here's how I did it.

The first thing I did was download my entire [Twitter Archive](https://support.twitter.com/articles/20170160). Your Twitter archive to allows you to browse a snapshot of your Twitter information, starting with your first Tweet. You get two things in your twitter archive:

* A fancy browsable local index.html website that opens up a JSON file of your tweet information
* A simpler CSV file of all your tweet information

For the purposes of creating this data visual I really just wanted the CSV. So with the CSV in hand I set about cleaning the dataset and isolating the only the data I was interesting, the number of tweets per day. I deleted all the columns of data I wasn't interested in (like individual TweetIds) to get down to just a list of tweets with timestamps.

The timestamps were in a `MM/DD/YYYY/00:00` format and since I was just interested in the day of a tweet left Excel and used [Atom's](https://atom.io/) multi cursor function to quickly delete the hour/minute information. (It's a neat little tick I learned for working with CSVs from my friend and coworker [Tom VanAntwerp](https://twitter.com/tvanantwerp])).

Once I was down to just the date timestamps for every tweet I did a simple [Count Individual Values](https://support.office.com/en-sg/article/Count-unique-values-among-duplicates-8d9a69b3-b867-490e-82e0-a929fbc1e273) function back in Excel. This gave me a count of the number of duplicates of unique values which of course is the number of tweets in any given day.

One histogram later here we are:

{% include image.html url="https://raw.githubusercontent.com/DanCarvajal/dancarvajal.github.io/7fd9dd2b6ef279fea3f0b4eb2f90d80f4a0475c6/images/Tweets_over_time.png" description="my tweets over time." %}

Some quick insights on the data:

* I have tweeted on 1,365 different days.
* My median number of tweets per day is 7 which seems about right when I look at my Buffer account which is set for minimum five tweets per day.
* I was interested in the outlier days where I tweeted a ton but they were actually just batch uploads of Facebook image albums thanks to IFTT.

This is just the start of diving into my Twitter data. Now I'm onto a harder task of pulling my Twitter engagement data from the Twitter API.
