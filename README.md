Hurricane Sandy on Flickr
===========

A site visualizing the use of Flickr tags related to [Hurricane Sandy](http://en.wikipedia.org/wiki/Hurricane_Sandy). It enables users to explore photos taken at before, during and shortly after the hurricane. Created as a project for [IO Lab, Fall 2012](http://courses.ischool.berkeley.edu/i290-iol/f12/).

## Project Team and Roles

* Naila Al-Khalawi - Visualization (using Google Charts) and design wiz
* [Dave Lester](http://davelester.org) - Flickr API magician and data cruncher

## Project Description
Our site has two main features:

* The ability to view (and compare!) the distribution of various tags over time that were used to tag photos of Hurricane Sandy. The total counts of these was queried prior to the launch of the site to avoid too many API calls at once (and they are unlikely to change much).
* Drilling down to specific points in time on the tag chart, and viewing photos that were taken and tagged. We're using the Flickr API to do this, ordering photos by the most-popular.

## Technologies Used

* Flickr API
* HTML, CSS, Javascript
* Google Charts API

## Our Process
We began with an interest visualizing, graphing, and/or exploring Flickr tags related to Hurricane Sandy. Since this project is thematically-organized (around the hurricane) and not a general purpose tool, we wanted to focus on a specific date range and a certain vocabulary.

The process of deriving the tags was trial and error at first. A vocabulary problem resulted in some photos being tagged ```flood``` while were tagged ```flooded``` -- we needed a solution. We considered importing all of these photo tags into a datastore to normalize their names, however the sheer number of photos that relate to the hurricane. Instead, we adopted a more manual approach by locating a [Hurricane Sandy Flickr Pool](http://www.flickr.com/groups/hurricanesandy/pool/) and analyzing the top 100 tags related to the storm. Using this information, we were able to find the top variations in spelling and tagging that occurred, and come up with the tags that we've visualized on our site. Through trial and error, we noticed that certain spelling variations had differing patterns of use, so for example we included both ```flood``` and ```flooding``` to illustrate this.

## Connection to Social Classification and its Usefulness
One of our driving questions was whether or not there was a relationship between the timing of events themselves and how they were socially classified. Would the tagging of photos be a useful way to see larger patterns of the storm?

For example, we wondered if we would notice a spike in different types of tagging at different points of the storm: first comes rain, then flooding. Our visualization confirms this initial hypothesis, which ties the tagging to the event itself.

## Lessons Learned
We learned that similar words may be used in varying ways. For example, the tag ```flooding``` spiked faster than ```flood```. After browsing some of the photos, it appears that flooding was used to tag the event of the flood itself (happening earlier), while flood was also used to describe the event of the flood itself. Many of the later flood photos are simply damage, with no visible water.

Technically, we learned to pay extra attention to API syntax. We were accidentally capitalizing one of the parameter in our original queries to Flickr, which was returning vastly different data. Luckily, we caught our mistake!