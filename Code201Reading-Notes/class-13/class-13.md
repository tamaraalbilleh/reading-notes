# THE PAST, PRESENT & FUTURE OF LOCAL STORAGE FOR WEB APPLICATIONS
## DIVING IN
* the operating system typically provides an abstraction layer for storing and retrieving application-specific data like preferences or runtime state
* These values may be stored in the registry, INI files, XML files, or some other place according to platform convention
* Cookies were invented early in the web’s history, and indeed they can be used for persistent local storage of small amounts of data.
## INTRODUCING HTML5 STORAGE
*  Web Storage, which was at one time part of the HTML5 specification proper, but was split out into its own specification for uninteresting political reasons.
* Certain browser vendors also refer to it as “Local Storage” or “DOM Storage.”
* cookies, this data persists even after you navigate away from the web site, close your browser tab, exit your browser, or what have you
* Instead of writing this function yourself, you can use Modernizr to detect support for HTML5 Storage.

## USING HTML5 STORAGE
HTML5 Storage is based on named key/value pairs
* You store data based on a named key, then you can retrieve that data with the same key. 
* The named key is a string. The data can be any type supported by JavaScript
* There are also methods for removing the value for a given named key, and clearing the entire storage area (that is, deleting all the keys and values at once).
* Finally, there is a property to get the total number of values in the storage area, and to iterate through all of the keys by index (to get the name of each key).
## TRACKING CHANGES TO THE HTML5 STORAGE AREA
* you can trap the storage event. 
* storage event is fired on the window object whenever setItem(), removeItem(), or clear() is called and actually changes something
## LIMITATIONS IN CURRENT BROWSERS
* “5 megabytes” is how much storage space each origin gets by default
* that you’re storing strings, not data in its original format.
## BEYOND NAMED KEY-VALUE PAIRS: COMPETING VISIONS
* new API has been standardized and implemented across all major browsers, platforms, and devices. As a web developer
*  An object store shares many concepts with a SQL database. There are “databases” with “records,” and each record has a set number of “fields.” Each field has a specific datatype, which is defined when the database is created.
