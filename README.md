# metaweather-cli
Simple Linux command line utility for displaying weather information using the [MetaWeather API](https://www.metaweather.com/api/).
## Overview
This utility displays weather information by using [curl](https://curl.haxx.se/) to retrieve information from the MetaWeather API in JSON form.
Relevant information is parsed from the JSON object using [jq](https://stedolan.github.io/jq/) and then formatted into a table using awk.
## Requirements
This utility runs in a Linux environment and requires three primary pieces of software in order to function:
* awk
* curl
* jq

The first two are usually included in most Linux distributions, but jq will most likely needs to be installed using your respective disto's package manager(e.g. `sudo apt install jq` for Debian/Ubuntu systems).
## Usage
To date this utility has three options:
* -q \[query term\]: retrieve WOEID(Where On Earth ID) numbers for list of locations returned by query term.
* -i \[woeid\]: display 6-day condition and weather forcast for location with coresponding WOEID.
* --help: displays a help page contain in accompanying file: *info.txt*.
## Future Development
#### -i Option
* [ ] Improve table generation.
* [ ] Add ability to display weather sources.
#### -q Option
* [x] Add option to display weather from list of locations/WOEIDs immediately after making a query. *Added October 30th, 2019*.
* [x] Add functionality to immediately display weather when only one location is returned from a query. *Added October 30th*, 2019.
## Notes
#### Known Issues
- Some valid WOEIDs will not return any data. This is due to the limitations of the MetaWeather API. An example of this is Reykjavík, Iceland(980389).
- Some data fields of the JSON objects returned from valid WOEIDs are incomplete due to lack of sources. Incomplete numeric fields are filled with placeholder values of 0/0.00.
#### Other
- All loating point values from JSON data are rounded to the nearest hundredth(#.##) in order to fit them into the current table stucture. 
## License
This program uses the GNU AGPL-3.0 License.