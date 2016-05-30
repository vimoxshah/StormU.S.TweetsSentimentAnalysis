# StormTweetsSentimentAnalysis
----------

## Features
* Application retrieves tweets from Twitter stream (using [Twitter4J](http://twitter4j.org)).<br>
* It analyses sentiments of the tweets from US.
* There are three different objects within a tweet that we can use to determine it’s origin. This application tries to find the location using all the three options and prioritizes location received in the following order [high to low]:
	* The coordinates object.
	* The place object.
	* The user object.
* For reverse geocoding, this application uses Bing Maps API.

* This application uses [AFINN](http://www2.imm.dtu.dk/pubdb/views/publication_details.php?id=6010), which contains a list of word with its pre-computed sentiment score.
	+ These words are used to determine sentiment of the tweets retrieved using Twitter Streaming API.
* While processing, after every 30 seconds [configurable], the application logs the sentiment values of the states to the console and simultaneously to a log file using Logback.<br>
* By understanding sentiment values, we can get the most happiest state of US and most unhappiest state as well.

