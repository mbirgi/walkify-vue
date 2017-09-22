# Walkify

Generates dynamic Spotify playlists paced for walking on the fly. This iteration is an android app made with Apache Cordova and Vue.js.

## Overview

This is an app that let's the user listen to tracks from his/her Spotify account (probably will have to have a premium account) while walking. The user is able to select a genre (and later maybe other parameters) and the app will start streaming music in the range of 120-130 bpm, which should be suitable for walking.


## Framework

The first iteration will be built from scratch, without using any frameworks, except for Angular. Later versions may be built with Ionic or any other framework that may seem suitable.

## Functional Design

> The main aim of this app is to be very simple to use, and to require only few clicks to get started and going. All tweaking will be done in "Advances Options" screens, sensible defaults should provide a pleasurable listening experience from the start.

### Required Functionalities

* Authenticate the user with Spotify
* Let user select one of 5 default genres
* Maintain a playlist of 10 reasonably popular tracks (when a track finishes playing, fetch a new one)
* Manage streaming from Spotify (Start/Stop/Pause/Restart playback, Skip to next (/previous) track)
* Display Artist and Track names

### Nice to Have Functionalities

* Avoid track duplication
* Let the user get a list of all available genres/moods and select one via incremental search
* Experiment with audio features to optimize stream:
  * loudness
  * danceability
  * energy
  * instrumentalness
  * liveness
  * valence
* Let user tweak additional parameters:
  * speachiness
  * acousticness
  * popularity
  * ...
* Display album cover
* Jump to track, artist, album in Spotify
* Save track
* Rate track
* Optimize stream according to user ratings of tracks

### Possible Future Features

* Get the user's 5 most listened genres from Spotify
* ability to fine tune the stream by liking/disliking tracks
* leveraging the user's existing Spotify history to optimize the stream
* last.fm support
* save playlists on Spotify
* save seed information for future walks
* use user's (online) library to select tracks from

## Technical Design

### Components
* Player (= App)

### Services
* Authentication
* Seed Selection
* Playlist Management
* Streaming
  
### Flow
* If user not logged in, authenticate and log in
* If no genre/mood selected, select seed
* Fetch a first playlist of 10 tracks
* Display track metadata
* Start streaming
* Enable and handle controls (play/pause/next/previous/stop)
