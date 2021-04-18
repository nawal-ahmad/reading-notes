# Readings : Audio, Video, Images


## Chapter 16: “Images” 


- We can control the size of image by `width:` and `height:`, and align them using `margin:` and `float:`.
- We can center an image 
````````
display: block ; 
margin: 0px auto;.
````````
- We can add image as background,
`background-image:url("link or relative path");`
`, you can control the background `background-repeat: ` or `background-attachment: `, to control background image position `background-position:`.

- We can change the image style when the mouse moved over the image(rollover) using `:hover`.

- To reduce the number of images that browser load, we can create image sprites.


## Chapter 19: “Practical Information” 

#### What is the definition of search engine optimization (SEO)?
It is the practice of trying to help site appear nearer the top of search engine results when people look for the topics that your website covers.

#### SEO Techniques:

- On page techniques:
    - Page Title: specified in the title.
    - URL / Web Address: use keyword in the file name.
    - Headings: keyword in heading element. `<h1>`
    - Text:repeat the keywords in the main body. 
    - Link Text: keywords create links between page.
    - Image Alt Text: accurate description of image help show it up in the result of image based searches 
    - Page Descriptions: lives inside the `<head>` element it's specify using `<meta>`.

- Off page techniques.

#### How to identify keywords and phrases?
to determine which keywords to use in the site we need to learn about the visitors and what they are looking for and at what point they are leaving and where are visitors coming from, by analytical tools such as Google Analytics.

- In order to put site on the web we need a domain name and web hosting.

- FTP programs allow transfer files from local computer to web server.



## Chapter 9: Flash

- Flash isvery popular technology used to add animations, video and audio to websites 
- Flash is not supported on iPhone or iPad and it'sno longer supported by many browsers too.


## Video and Audio APIs

- To embed video and audio in web pages we can apply them to your page by using the `<video>` and `<audio>` elements.

- To control video and audio players we used `HTMLMediaElement.play()` and `HTMLMediaElement .pause()`.

- We need to wrap audio and video elements in `div` to style them if needed.

- Video elements contains two `<source>`so different format can be loaded depending on the browser.

- There is for `<button>` to control video and audio play, pause, stop and fast forward.

- `<span>` containing the elapsed time in minutes and seconds.

- Control visibility, opacity of videos and audios by CSS.


- Implementing videos and audios the JavaScript using by: 
1. creat new JavaScript file in the same directory.
2. insert specific code.

- We use event listener to stop and play the video or the audio (ex. `play.addEventListener(action, function)`).

- We can move video and audio forward and backward, fixing play and pause by (`fwd` and `rwd`).





