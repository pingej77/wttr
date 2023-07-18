# wttr
Front end tool for text weather app wttr.in for the Linux command line

https://wttr.in is a text-based weather website that can be fetched with curl.
This script calls wttr.in and also allows you to set a default locale, pass options using a more traditional syntax, and makes it a little bit quicker to type.  Otherwise, it has most of the same functionality as wttr.in.

When passing no options to wttr.in, it will often provide a best guess that is quite inaccurate.  Instead, set a default locale so you don't have to type a locale every time.<br>
Do this with the -d option:
`wttr -d "New York"` &emsp; (quotes are necessary if locale is more than one word)<br>
To get the weather for other locales, simply type the name (quotation marks are not necessary and spaces are accepted), ex:
`wttr New York`

Unit options are:<br>
-m, -c, and -C to use Celsius/metric.  -M uses Celsius and displays wind-speed in m/s instead of km/h. <br>
-u, -f, and -F use Fahrenheit and mph for wind speed (US std units)

-n makes the display narrow, -0 only displays current weather, -1 only displays today, and -2 only displays today and tomorrow

Sometimes wttr.in is a bit finnicky when it comes to returning the right locale.  For example, 'st petersburg' loads St. Petersburg, Florida, while 'St.Petersburg' and 'Saint Petersburg' load St. Petersburg, Russia; Telaviv will load Rua Telaviv, Brasil, while 'Tel Aviv' will return Tel Aviv, Israel.
Locations can typically be in a variety of languages, i.e., Cologne, Colonia, Koln or Moscow, Москва, Moskau. 
Three letter airport codes can be used as well to get weather information.

To install, run the following:

```bash
sudo curl -o /usr/local/bin/wttr https://raw.githubusercontent.com/pingej77/wttr/main/wttr && sudo chmod +x /usr/local/bin/wttr
```

If it doesn't work, just add the main 'wttr' file to somwhere in your $PATH such as /usr/local/bin/ and mark it as executable with `chmod +x wttr`

Just a small bash script. Enjoy!
