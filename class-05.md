# Read: 05 - HTML Images; CSS Color & Text

## Duckett HTML book:

### Chapter 5: “Images”

- Images can improve the design and the appearance of a web page.

- To embed an image in the web page we used `<img>` tag, 
`<img src="url" alt="alternatetext">`
  
- src - the path of the image
- alt - alternate text for the image

- Style image by specify the width and height attrributes.

- Use the CSS float property to let the image float and align property to alligning image horizontally (right,left) and vertically (top, middle, bottom)

- Rules for creating images:
    - save image in the right format
    - save image at the right size
    - use the correct resolution 72 ppi.

- Use a `<figure>` specifies self-contained content, like illustrations, diagrams, photos, etc. 
- `<figcaption>` element used to defines a caption for a `<figure>` element.

### JPEG vs PNG vs GIF — which image format to use and when?

- JPEG: a lossy compression format used for all photograph where variation in colour and intensity is smooth. 
- PNG: a lossless image format used for any image that needs transparency or for images with text & objects with sharp contrast edges like logos. 
- GIF: a lossless image format used for images that contain animations.
- all forms of data are compressed to reduce the size and faster.
- Compression can be of two types 
    - lossless there is a possible to reconstruct the original image from the compressed image 
    - lossy

- Transparency
    - JPEG images don’t support transparency
    - PNG images support transparency in two ways, 
        - an alpha channel 
        - index transparency
    - GIF images support transparency by index transparency
- Colors
    - JPEG images can support around 16 million colours.
    - PNG: PNG8 can support upto 256 colours whereas PNG24 can handle upto 16 million colours 
    - GIF: limited to 256 colours.
- Animation
  - any change or movement in the image.
  - only GIF supports animation


### Chapter 11: “Color” 

- Color can really bring your pages to life.

- Colors in CSS can be specified by the following methods:
  - RGB values
  - Hexadecimal codes
  - color names

- An RGB color value is specified with the rgb() function, which has the following syntax:

  rgb(red, green, blue), each parameter defines the intensity of the color.

- A hexadecimal color is specified with: #RRGGBB, where the RR (red), GG (green) and BB (blue) hexadecimal integers specify the components of the color. All values must be between 00 and FF.

- ِAppropriate contrast between any text and the background color is important.

- The rgba() function define colors using the Red-green-blue-alpha (RGBA) model, where is alpha defines the opacity as a number between 0.0 (fully transparent) and 1.0 (fully opaque).

- The hsla() function define colors using the Hue-saturation-lightness-alpha model (HSLA).
  - Hue is a degree on the color wheel from 0 to 360. 0 is red, 120 is green, and 240 is blue.

  - Saturation is a percentage value, 0% means a shade of gray, and 100% is the full color.

  - Lightness is also a percentage, 0% is black, 50% is neither light or dark, 100% is white


### Chapter 12: “Text” 

- We have two types of text markup:
  1. Structural markup: the elements that use to describe headings and paragraphs
    - Headings from h1 (main heading) to h6.
    - Paragraphs `<p>`
    - Bold `<b>` & Italic `<i>`
    - Superscript `<sup>` superscript & Subscrip `<sub>` subscript.
    - White Space to make code easier to read.
    - Line Breaks `<br/>` (new line) & Horizontal Rules `<hr/>` (break between theme)
  2. Semantic markup: which provides extra information like where emphasis should be placed, and others.
    - `<strong>` used to define text with strong importance.
    - `<em>` used to define emphasized text.
    - `<blockqoute>` used to tag specifies a section that is quoted from another source.
    - `<q>` used for shorter quotes that sit within a paragraph.
    - `<abrr>` use an abbreviation or ancronym.
    - `<cite>` defines the title of a creative work.
    - `<dfn>` used to indicate the defining instance of a new term.
    - `<address>` defines the contact information for the author/owner of a document or an article.
    - `<ins>` e used to show content that has been inserted into a document.
    - `<del>` n show text that has been deleted from it.
    - `<s>` indicates something that is no longer accurate or relevant.

