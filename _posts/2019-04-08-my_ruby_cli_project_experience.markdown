---
layout: post
title:      "My Ruby CLI Project Experience:"
date:       2019-04-08 04:53:31 +0000
permalink:  my_ruby_cli_project_experience
---



To say this was challenging for me would be an understatement. Having zero background in coding aside from bootcamp pre-work and basic HTML manipulation on Myspace back in the day, I have been flooded with new infomation over the past few weeks. While the labs can be challenging, the built in tests offer valuable insight to how your code is running and what needs to be fixed. Flying solo was a horse of a different color. 

The video walk-throughs were incredibly useful in completeing this project as they provided the outline for scraping a website using Open-URI and Nokogiri to parse the HTML document to extract deisred data using CSS Selectors. My project provides the user with a list of common reasons for practicing yoga (Anxiety, Fitness, Sciatica, etc) and asks for their selection. Upon selection, the user is provided by a list of postures from which he will benefit most. If the user chooses, he may return to the list of reasons for practicing to acquire a new list of postures, or may drill into a specific posture from their original selection for more information, including step-by-step instructions. 

The first part of the scraping went well. Grabbing and listing the reasons for practicing went off without a hitch. AWESOME! I was feeling pretty good. But wait, there's more.... As I began scraping the next level for a list of postures, I ran into a slight problem with duplicate values from articles at the bottom of the page. By chaining an additional, more specific CSS selector, I was able to eliminate the duplicates. Perfect. Now I have a list of postures for each of the common reasons to practice yoga. All I need now is detailed information about the specific asana. I begin examining the HTML and CSS selectors. It was definitely not a pretty process as the CSS was not conducive to scraping with very little specificity between elements. I had to do a little bit of hard coding to factor out unneeded information. I'm looking forward to diving further in to look at more elegant solutions. 

On Friday afternoon, I went to lunch (CLI running) with a couple of friends. When I came back and ran my code (no changes made), I received a SocketError. After researching what in the heck a SocketError was, I couldn't find a better solution that rebooting to start. Presto! Back in business.
 
I had Yoga Teacher Training from 9-5 on Saturday and Sunday. Needless to say, those days leave me a bit exhausted and brain functioning at 100%. Having never used github other than to clone a repo to learn, this evening has been incredibly frustrating for me. I made an error early on in the file path that took me longer than I care to admit to identify.  Now, here we are. 

My first project completed in a completely new field, far different than anything I have ever done. What I found in completeing the CLI project is that currently, big picture concepts make sense, but are not always executable. In other words, I feel I can read adequately, but writing is going to take a bit more practice. I am enjoying being challenged on a daily basis. I have learned a vast amount already and am excited to continue this process.
