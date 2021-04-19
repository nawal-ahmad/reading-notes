# Local Storage

### LOCAL STORAGE HACKS BEFORE HTML5


- Cookies can be used for persistent local storage of small amounts of data. 

- Cookies are included with every HTTP request, It's slowing down the web application, sending data unencrypted over the internet

- Before HTML5 5 userData allows web pages to store up to 64 KB of data per domain. 

- Flash cookies allows Flash objects to store up to 100 KB of data per domain.

- Gears can store unlimited amounts of data per domain in SQL database tables. 

### HTML5 STORAGE

#### what is HTML5 Storage?  
it’s a way for web pages to store named key/value pairs locally within the client web browser, this data persists even after navigate away from the web site, close the browser tab, exit the browser unlike cookies mentioned before.

- HTML5 Storage is based on named key/value pairs. storing data based on a named key and retrieve that data with the same key. _(The named key is a string._ 

- The data can be any type supported by JavaScript, including (strings, Booleans, integers, or floats), the data stored as a string.

- As mentioned before in our classes to store and retrieve anything other than strings we use functions like parseInt() or parseFloat() to coerce your retrieved data into the expected JavaScript datatype.

- The storage event is fired on the window object whenever setItem(), removeItem(), or clear() is called and actually changes something. 

- 5 megabytes” is how much storage space each origin gets by default in the current browser.


Rerefence:
[The Past, Present, and Future of Local Storage for Web Applications](http://diveinto.html5doctor.com/storage.html)