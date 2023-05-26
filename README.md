[![License](https://img.shields.io/github/license/dolbyio-samples/blog-browser-getting-started-media-device-picker)](LICENSE)

![Blog Picture](https://dolby.io/wp-content/uploads/2021/12/DolbyIO-mute-desktop.jpg)

# Dolby.io Video Conference Application with Media Devices Controls
Adds a selection menu to choose a microphone, camera, and speaker from the list of media devices that can be controlled by the browser.

# Overview
[This blog](https://dolby.io/blog/adding-a-media-device-selection-menu-for-picking-camera-and-microphone/) focuses on utilizing the Communication API to enable control over media devices in video conferencing applications, empowering end-users to manage and switch their devices during conferences.

# Requirements
You will need four items for this tutorial: a [Dolby.io account](https://dolby.io/), a working webcam, a speaker, and a microphone. 

# Getting Started
Here is how to set up and run this project locally.

### Prerequisites
* Sign up for a free Dolby.io account [here](https://dashboard.dolby.io/).
* Create a new application and save the Communications API key and secret.

### Installation and Usage
1. Clone this repo and change directory.
    ```sh
    $ git clone https://github.com/dolbyio-samples/blog-browser-getting-started-media-device-picker

    $ cd blog-browser-getting-started-media-device-picker
    ```
    
2. Replace this line in [client.js](./src/scripts/client.js) with your Dolby.io Communications API key and secret.
    ```js
    VoxeetSDK.initialize('customerKey', 'customerSecret');
    ```
    
3. Start a simple http server to access the conference web application
    ```sh
    $ cd src && npx http-server -a localhost -p 8000 -c-1 -o ./

4. Open the application in your web browser at [localhost:8000](http://localhost:8000).


### Why Start a HTTP Server?
Chrome has [deprecated](https://www.chromium.org/Home/chromium-security/deprecating-powerful-features-on-insecure-origins) support for accessing media devices through insecure origins (`http://`) and visiting a local web page through it's HTML file is not recognized as a secure origin (`https://`). However, you can test the Communications API's media devices feature through your machine's localhost since it is treated as a secure origin on Chrome and other Chromium browsers.

Safari on macOS (as of [v15.0](https://developer.apple.com/documentation/safari-release-notes/safari-15-release-notes)) still supports accessing media devices through insecure origins, so you can open the [index.html](./src/index.html) file on there without starting a HTTP server for testing purposes.

# Report a Bug 
In the case any bugs occur, report it using Github issues, and we will see to it. 

# Forking
We welcome your interest in trying to experiment with our repos.

# Feedback 
If there are any suggestions or if you would like to deliver any positive notes, feel free to open an issue and let us know!

# Learn More
For a deeper dive, we welcome you to review the following:
 - [Communications API](https://docs.dolby.io/communications-apis/docs)
 - [Getting Started with Web SDK](https://docs.dolby.io/communications-apis/docs/getting-started-with-the-javascript-sdk)
 - [Deliver Video Conference Recordings with Webhooks and AWS Lambda](https://dolby.io/blog/deliver-video-conference-recordings-with-webhooks-and-aws-lambda/)
 - [How-to Build a Video Call App for Music Lessons or Live Performances](https://dolby.io/blog/build-a-video-call-app-for-music-lessons-or-live-performances/)
 - [How to Remove Background Noise from Audio](https://dolby.io/blog/how-to-remove-background-noise-from-audio/)

# About Dolby.io
Using decades of Dolby's research in sight and sound technology, Dolby.io provides APIs to integrate real-time streaming, voice & video communications, and file-based media processing into your applications. [Sign up for a free account](https://dashboard.dolby.io/signup/) to get started building the next generation of immersive, interactive, and social apps.

<div align="center">
  <a href="https://dolby.io/" target="_blank"><img src="https://img.shields.io/badge/Dolby.io-0A0A0A?style=for-the-badge&logo=dolby&logoColor=white"/></a>
&nbsp; &nbsp; &nbsp;
  <a href="https://docs.dolby.io/" target="_blank"><img src="https://img.shields.io/badge/Dolby.io-Docs-0A0A0A?style=for-the-badge&logoColor=white"/></a>
&nbsp; &nbsp; &nbsp;
  <a href="https://dolby.io/blog/category/developer/" target="_blank"><img src="https://img.shields.io/badge/Dolby.io-Blog-0A0A0A?style=for-the-badge&logoColor=white"/></a>
</div>

<div align="center">
&nbsp; &nbsp; &nbsp;
  <a href="https://youtube.com/@dolbyio" target="_blank"><img src="https://img.shields.io/badge/YouTube-red?style=flat-square&logo=youtube&logoColor=white" alt="Dolby.io on YouTube"/></a>
&nbsp; &nbsp; &nbsp; 
  <a href="https://twitter.com/dolbyio" target="_blank"><img src="https://img.shields.io/badge/Twitter-blue?style=flat-square&logo=twitter&logoColor=white" alt="Dolby.io on Twitter"/></a>
&nbsp; &nbsp; &nbsp;
  <a href="https://www.linkedin.com/company/dolbyio/" target="_blank"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white" alt="Dolby.io on LinkedIn"/></a>
</div>


