# metaweather-cli
Simple Linux command line utility for displaying weather information using the MetaWeather API.
## Overview
This utility displays weather information by using [cURL](https://curl.haxx.se/) to retrieve information from the MetaWeather API in JSON form.
Relevant information is parsed from the JSON object using [jq](https://stedolan.github.io/jq/) and then formatted into a table using awk.
