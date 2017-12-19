.. fmwsdata documentation master file, created by
   sphinx-quickstart on Tue Dec 19 16:46:00 2017.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to fmwsdata's documentation!
====================================

Contents:

.. toctree::
   :maxdepth: 2



Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`


TwitterGeoCrawler
=================

-  Running on fmedia12 (cron job)
-  Files stored in fmedia7 (``/scratch0/fmedia12_export/.../JSONstore``)
-  Data stored on fmedia7 (as of Dec 2017): 428G
-  Size of daily collection (lzo compressed): ~1G


TwitterStream
=============

- Collection of Python 2x apps using Tweepy v3.5 (documentation_)
- Running on fmedia15 (supervisord managed service)
- Stream saved to file every hour
- Files moved to fmedia7 every hour (cron job)
- Hourly files are lzo compressed every night (cron job)

.. _documentation: http://tweepy.readthedocs.io/en/v3.5.0/

fluterms/fluwords
-----------------

- Files stored locally and then moved to fmedia7 (`/scratch0/fmedia12_export/.../twitterStream/fluwords`)
- Data stored on fmedia7 (as of Dec 2017): 1.1T 
- Size of daily collection (lzo compressed): ~1G
- Uses a list of 114 flu-related words in English and Danish as a filter
- Resource URL https://stream.twitter.com/1.1/statuses/filter.json

.. raw:: html

  <script src="https://gist.github.com/david-guzman/522aa123de5cf52618fb0fa0a95f3659.js"></script>


geofilter
---------

- Files stored locally and then moved fmedia7 (`/scratch0/fmedia12_export/.../twitterStream/geofilter`)
- Data stored on fmedia7 (as of Dec 2017): 1.2T 
- Size of daily collection (lzo compressed): ~250M
- Uses a list of location coordinates as a filter `-9.23, 49.84, 2.69, 60.85, 8.075, 54.559, 15.193, 57.7519`
- Resource URL https://stream.twitter.com/1.1/statuses/filter.json

.. raw:: html 

  <script src="https://gist.github.com/david-guzman/1174cf2904f040c36ea5ecc0cc9eeb1f.js"></script>


sample
------

- Files stored locally and then moved fmedia7 (`/scratch0/fmedia12_export/.../twitterStream/sample`)
- Data stored on fmedia7 (as of Dec 2017): 1.8T 
- Size of daily collection (lzo compressed): ~4G
- Collects a small random sample of all public stata as provided by `Twitter Streaming API`_
- Resource URL https://stream.twitter.com/1.1/statuses/sample.json

.. _Twitter Streaming API: https://developer.twitter.com/en/docs/tweets/sample-realtime/api-reference/get-statuses-sample

.. raw:: html 

  <script src="https://gist.github.com/david-guzman/65d8c604b9b4f418d6d52051c3c9b905.js"></script>
