# metaweather-cli
Simple Linux command line utility for displaying weather information using the MetaWeather API.
## Overview
This utility displays weather information by using [curl](https://curl.haxx.se/) to retrieve information from the MetaWeather API in JSON form.
Relevant information is parsed from the JSON object using [jq](https://stedolan.github.io/jq/) and then formatted into a table using awk.
## Requirements
This utility runs in a Linux environment and requires three primary pieces of software in order to function:
* awk
* curl
* jq

The first two are usually included in most Linux distributions, but jq will most likely needs to be installed using your respective disto's package manager(e.g. `sudo apt instal jq` for Debian/Ubuntu systems).