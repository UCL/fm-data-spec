data-collection-spec
====================

Documentation and specification for data collection from Twitter and
Google

TwitterGeoCrawler
=================

-  Running on fmedia12 (cron job)
-  Files stored in fmedia7 (``/scratch0/fmedia12_export/.../JSONstore``)
-  Data stored on fmedia7 (as of Dec 2017): 428G
-  Size of daily collection (lzo compressed): ~1G

::

test


TwitterStream
=============

- Collection of Python 2x apps using Tweepy v3.5 (http://tweepy.readthedocs.io/en/v3.5.0/[documentation])
- Running on fmedia15 (supervisord managed service)
- Stream saved to file every hour
- Files moved to fmedia7 every hour (cron job)
- Hourly files are lzo compressed every night (cron job)

fluterms/fluwords
-----------------

- Files stored locally and then moved to fmedia7 (`/scratch0/fmedia12_export/.../twitterStream/fluwords`)
- Data stored on fmedia7 (as of Dec 2017): 1.1T 
- Size of daily collection (lzo compressed): ~1G
- Uses a list of 114 flu-related words in English and Danish as a filter
- Resource URL https://stream.twitter.com/1.1/statuses/filter.json

::

test


geofilter
---------

- Files stored locally and then moved fmedia7 (`/scratch0/fmedia12_export/.../twitterStream/geofilter`)
- Data stored on fmedia7 (as of Dec 2017): 1.2T 
- Size of daily collection (lzo compressed): ~250M
- Uses a list of location coordinates as a filter `-9.23, 49.84, 2.69, 60.85, 8.075, 54.559, 15.193, 57.7519`
- Resource URL https://stream.twitter.com/1.1/statuses/filter.json

<script src="https://gist.github.com/david-guzman/1174cf2904f040c36ea5ecc0cc9eeb1f.js"></script>


sample
------

- Files stored locally and then moved fmedia7 (`/scratch0/fmedia12_export/.../twitterStream/sample`)
- Data stored on fmedia7 (as of Dec 2017): 1.8T 
- Size of daily collection (lzo compressed): ~4G
- Collects a small random sample of all public stata as provided by https://developer.twitter.com/en/docs/tweets/sample-realtime/api-reference/get-statuses-sample[Twitter Streaming API]
- Resource URL https://stream.twitter.com/1.1/statuses/sample.json





`
