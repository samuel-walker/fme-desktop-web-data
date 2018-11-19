# Using Web Data with FME Desktop

This repo contains an example of using FME to stream tweets and display them in a Leaflet web map. It can be adapted for use with FME Server and hosting on the web, but here is presented without using FME Server for ease of use for beginners.

# Set up

1. Ensure FME Desktop 2019.0 or newer is installed.
2. Run [fme\TweetStreamer.fmw](fme\TweetStreamer.fmw). You can fill in prompted values to set a single search keyword.
  - Note that Tweetstreamer.fmw will run until manually stopped.
3. Run [fme\TweetFilter.fmw](fme\TweetFilter.fmw). This workspace takes the streaming Tweets and displays them in a Leaflet web map.
4. To see the web map, you must set up a local HTTP server.

To view the example, run a local HTTP server in this folder. If you have Python 2.x installed, you can start a server by opening your terminal and entering

`python -m SimpleHTTPServer`

If you have Python 3.x installed, this will work instead:

`python -m http.server`

Your map will now be accessible from [http://localhost:8000/](http://localhost:8000/).
