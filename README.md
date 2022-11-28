# adsb-flightalert

This little Python module will let you parse an aircraft.json file from a running dump1090 instance and return a list with all flights that match a certain (single, for now) criteria.

You can filter based on any key found in an aircraft record. For example

squawk = 7700 or callsign = blah

There is one main function, parseJSONfile() - send it three strings:

* the path to the aircraft.json file including trailing slash (like /run/dump1090-fa/ for example)
* the filter text to search for, such as "7700"
* the key name to search in, such as "squawk"

Hits are logged to stdout every time they are detected right now. I may change this.

An example script is provided to show how to use it with some basic logic to help suppress alert spam. You should get an idea of how to use the library with it.

Set up a main loop, sleep for a time delay (check as often as you deem necessary), set a variable with the results of the parsing function and then do what you want with the returned data. Use your imagination!
