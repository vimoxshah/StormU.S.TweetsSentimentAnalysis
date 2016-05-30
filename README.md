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
	* For more information and sign up, please check [Getting Started with Bing Maps](http://msdn.microsoft.com/en-us/library/ff428643.aspx).
	* Please note that you would need Windows Live account for signing up for Bing Maps API key.
	* Also, please consider opting for Basic Plan for Bing Maps API, as that is better for our usage. As of 18th June, 2013, limit is 50k requests for 24 hours in Basic Plan.
	* I chose Bing Maps and not Google Maps since Google Maps is too restrictive for our usage, as it has a limit of only 2500 requests per day, which is too small a threshold for our work.
* This application uses [AFINN](http://www2.imm.dtu.dk/pubdb/views/publication_details.php?id=6010), which contains a list of word with its pre-computed sentiment score.
	+ These words are used to determine sentiment of the tweets retrieved using Twitter Streaming API.
* While processing, after every 30 seconds [configurable], the application logs the sentiment values of the states to the console and simultaneously to a log file using Logback.<br>
* By understanding sentiment values, we can get the most happiest state of US and most unhappiest state as well.

