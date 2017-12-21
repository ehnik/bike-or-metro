This application allows users to enter weather requirements for their mode of commute. According to their preferences, they will be shown whether they should bike or take the metro.

The React/Flux code in this application is my own; the configuration files are inherited from a template.


Please see below for additional information about the files I created in this directory

#Weather.js
>Since the app can't function without a response from the API, I had it initialize
the weather store once the API call is successful. This provides an easy way to show
a pending status in the header and to prevent a bug from occurring when the user submits
their commute preferences.

#WeatherActions.js
>Both high temp and low temp are passed on to the store; if the data is hourly,
both variables have the same value. This made calculating the preferred mode of
transportation more efficient, given the possibility of either daily
or hourly weather data in the store.

#set-commute-time.js
>This function takes as an argument the unix timestamp returned by the store's
weather data. I had it do this (rather than just calculating based
on the current time) for both efficiency and to give greater transparency
in case the wrong hour was somehow calculated for the hourly weather data in
the store.

#utils folder
>I extracted a few functions and put them in here so they could easily be re-used
and tested.
