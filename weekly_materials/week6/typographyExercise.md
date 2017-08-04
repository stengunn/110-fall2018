# Typography Exercise 

## Overview & Goals
In today's exercise, you'll use CSS to modify the typography on an HTML page. 

If you complete the exercise before the start of class on Thursday, you do not need to come to class. We will take attendance, and check the URL referenced above for anyone who isn’t in class. If the exercise is accessible and has been properly completed, you’ll get full credit for the exercise and for attendance. If it is not accessible, or was not properly completed, you’ll get no credit for attendance, and a zero on the exercise. 

## Creating Your Work Files
Create a folder called `typography` in your local copy of the igme110 folder. Using Visual Studio (or the text editor of your choice), create a new html 5 file called fonts.html and save it to the typography folder.

Leave the fonts.html file open, and create another new file called fonts.css. 

You should now have two tabs open in your editor. 

# Adding Content to the HTML Page
You need enough text on the page to be able to see the effects of changing aspects of the typography. At a minimum, you should have two different types of headings (e.g. `<h1>` and `<h2>`), two paragraphs of text, and at least one blockquote. Each of the paragraphs and the blockquote should have a full paragraph of text in them. If you don’t feel like writing your own text, you can use a “lorem ipsum” filler text generator; several can be found here: http://www.macobserver.com/tmo/article/10-great-alternative-lorem-ipsum-filler-text-generators. 

You also need to link the fonts.css stylesheet file to your html document, using a link tag in the head of your document: `<link rel="stylesheet" href="fonts.css">`. (In VS Code, you can use Emmet to create the structure of the tag by typing `link:css` and pressing tab.) 

Here's generally what the document ought to look like when you preview it in a browser (although you may have your blockquote in a different location):

![Unformatted Fonts Page](fontsPage1.png)

# Adding CSS Formatting
After each of the steps below, save your fonts.css file and then reload fonts.html in the browser, so you can see the effect of your changes. 

In your fonts.css file, add a line to change the font family for the h1 elements. Choose a font family that is likely to work across platforms—there’s a list of cross-platform fonts available at http://web.mit.edu/jmorzins/www/fonts.html. The serif font Georgia and the sans-serif font Verdana were designed specifically for web readability, so if you’re not sure what to use, choose one of those. 

As a reminder, in your CSS file, you’d change the font for h1 elements like this, where *fontname* is the font you've chosen:
```css
h1 { font-family: "fontname"; }
```
(The quotes around the font name are only necessary if the font has a space in its name.)

Next choose a font-family for the p tag, and specify that in the CSS file, as well. 

Using the font-size property, change the size of the text in the paragraph tag. CSS properties can be specfied as an absolute value using pixels, points or ems, or as a percentage value. For paragraph text, a value between 12px and 16px probably makes the most sense. As a reminder, you can have multiple CSS declarations for one tag, and you can include line breaks within your definitions, so you could have something like this:

```css
p { 
    font-family: “fontname”; 
    font-size: value; 
    }
```

You can assign styles to more than one HTML tag at a time, by separating the tags with commas. Try assigning the same font attributes to the p and the blockquote tag, like this:
```css
 p, blockquote { 
    font-family: “fontname”; 
    font-size: value; 
    }
```

Using the line-height property, add another line to the definition for p and blockquote, changing the line spacing. I recommend using 150% as the value, but you can play around with different values (using percentage, point, or pixel values) to see how it looks. 

Finally, try changing the width of all the content now, by adding a width property for the body of the document:
```css
     body { width: value; }
```
Try specifying a relative width using a percentage value (70% or 80%), and then view the file and try resizing the browser window. Note what happens. Then change the width specification to a fixed pixel value (600px or 800px) and try the same thing. Leave it set to a fixed width. 

## Using Google Fonts 

Google provides a number of high-quality typefaces available online for anyone to link to in their CSS. Go to http://www.google.com/fonts/ to see what’s available, and browse through the fonts. Then go to https://developers.google.com/fonts/docs/getting_started for instructions on how to incorporate these hosted typefaces into your own pages. 

Identify a typeface you’d like to use for heading on your page, and update  your HTML and CSS files to use the selected typeface for your h1 and h2 elements. (Feel free to use Google fonts for other elements in the page, but you’re only required to use them for the headings.) You can either add the Google Font using a link element in your HTML document, or by using an @import rule in your CSS. 

Here's an example of the font being added with an @import rule in the CSS, and the resulting page formatting:
![Google Fonts Code](googleFontsCode.png)
![Google Fonts Page](googleFontsPage.png)


## Adding Character Entities 

Add a level 2 heading of "Words of Wisdom" to the end of the document.

Under the heading, add a blockquote enclosing a quote that you particularly. Enclose the text of the quote with opening and closing quotation marks (curly or "smart") quotes using HTML character entities.

Below the quote, add the attribution for who said it, preceding the name with a typographic em dash (again, using the appropriate HTML entity). 

It should look like this when you're done:

![Screenshot Showing HTML Entities](htmlEntities.png)

## Submitting Your Work 
Use an FTP client to upload the typography directory and its contents to the igme110 directory in your www directory on Banjo. We’ll check http://people.rit.edu/~youruserid/igme110/typography/fonts.html to see if you’ve completed the exercise. Make sure you test that URL to ensure that the files appear properly and can be loaded in a browser! 

If you choose to work on this on your own, and not attend class on Thursday, your work must be completed and accessible by the start of class that day. 

If you do attend class on Thursday, and are not able to complete the work before the end of class, you'll have until Saturday at noon to turn it in. 



