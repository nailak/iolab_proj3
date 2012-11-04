Hurricane Sandy on Flickr
===========

A site visualizing the use of Flickr tags related to [Hurricane Sandy](http://en.wikipedia.org/wiki/Hurricane_Sandy). It enables users to explore photos taken at before, during and shortly after the hurricane.

## Project Team and Roles

* Naila Al-Khalawi - Visualization and design wiz
* [Dave Lester](http://davelester.org) - Data cruncher and API magician

## Project Description
Our site has two main features:

* The ability to view (and compare!) the distribution of various tags over time that were used to tag photos of Hurricane Sandy. The total counts of these was queried prior to the launch of the site to avoid too many API calls at once (and they are unlikely to change much).
* Drilling down to specific points in time on the tag chart, and viewing photos that were taken and tagged. We're using the Flickr API to do this, ordering photos by the most-popular.

## Our Process=
We began with an interest visualizing, graphing, and/or exploring Flickr tags related to Hurricane Sandy. Since this project is thematically-organized (around the hurricane) and not a general purpose tool, we wanted to focus on a specific date range and a certain vocabulary.

The process of deriving the tags was trial and error at first. A vocabulary problem resulted in some photos being tagged 'flood' while were tagged 'flooded' -- we needed a solution. We considered importing all of these photo tags into a datastore to normalize their names, however the sheer number of photos that relate to the hurricane. Instead, we adopted a more manual approach by locating a [Hurricane Sandy Flickr Pool](http://www.flickr.com/groups/hurricanesandy/pool/) and analyzing the top 100 tags related to the storm. Using this information, we were able to find the top variations in spelling and tagging that occurred, and come up with the tags that we've visualized on our site.

The step of analyzing tagging behavior was critical because it shifted our approach to querying tags. We originally looked only for images tagged ```sandy```, but learned that ```hurricane``` and ```hurricanesandy``` were also common tags. By limiting the photos to those that were taken on specific dates, we were hopefully able to minimize the number of tags meant to describe other hurricanes.