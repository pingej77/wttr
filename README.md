# wttr
Front end tool for command line weather app wttr.in

https://wttr.in is a text-based weather website that can be fetched with curl.
It allows you to set a default locale, pass options using a more traditional syntax, and makes it a little bit quicker to type.  Otherwise, it has most of the same functionality as wttr.in.

When passing no options to wttr.in, it will often provide a best guess that is quite inaccurate.  For this reason, setting a default locale is sensible so you don't have to type it in every time.
Do this with the -d option:
`wttr -d "New York"`
To get the weather for other locales, simply type the name (quotation marks are not necessary and spaces are accepted), ex:
`wttr New York`

Unit options are:
-m, -c, and -C to use Celsius/metric.  -M uses Celsius and displays wind-speed in m/s instead of km/h.  
-u, -f, and -F use Fahrenheit and mph for wind speed (US std units)

-n makes the display narrow, -0 only displays current weather, -1 only displays today, and -2 only displays today and tomorrow

Sometimes wttr.in is a bit finnicky when it comes to returning the right locale.  For example, 'st petersburg' loads St. Petersburg, Florida, while 'St.Petersburg' and 'Saint Petersburg' load St. Petersburg, Russia; Telaviv will load Rua Televiv, Brasil, while 'Tel Aviv' will return Tel Aviv, Israel.
Locations can typically be in a variety of languages, i.e., Cologne, Colonia, Koln or Moscow, Москва, Moskau. 
Three letter airport codes can be used as well to get weather information.

Just a small script, enjoy!