# Basic HTML & CSS Exercise 

## Overview & Goals

In today's exercise, you'll use Visual Studio Code to create some web pages, adding basic CSS formatting, and uploading it to your RIT web space. 

We will also be adding a configuration file to your RIT web space to override some of the server's (problematic) default behavior.

## Setting Up Your Folders and Files

On your computer (or on a USB drive) create a folder called banjo. Inside of the banjo folder, put a folder called www . Inside of the www folder, put a folder called igme110. And inside of the igme110 folder, put folder called media. The www folder represents your www directory on banjo.rit.edu. The igme110 folder is where all of your exercises and projects for this class will be stored.  


## Setting Up VS Code

While you can use Visual Studio Code to open and edit a single file, it works best if you start by pointing it to your working folder. Launch the program, and then choose "Open Folder..." from the File menu. Find the igme110 folder you just created on your local or USB drive, and and open it. 

## Creating Your Class Home Page

Choose "New File" from either the welcome page (if it's displayed) or from the File menu.   

Save the blank file with the name "index.html" in the igme110 folder. The file extension does two things--first,it tells VS Code that you want to use HTML syntax in the file, and second, after it's been uploaded it tells the web server how to process the file when it's requested. 

Now you're going to use one of VS Code's built-in HTML tricks, which is powered by an addon called "Emmet". Type `html:5` on the first line of the document (don't add any spaces or new lines after it), and then press tab. You should see a full HTML 5 document structure appear in the file. 

In the head of the document, add this content to the title tag (using your name, of course):
```<title>Elizabeth Lawley's IGME 110 Page</title>```

In the body of the document, add a level 1 heading tag (`<h1></h1>`) and put your name in it. Below that, add a paragraph (`<p></p>`) that includes a few lines about yourself. Save the file. 

Open a web browser, and in the browser use the File-->Open command to locate and display the index.html file you just created. It should look something like this:

![index.html with h1 and p content](110homepage-1.png) 

## Adding an Image

Part  2:  Adding An Image

Find a Creative Commons-licensed image on the web, or an image that you’ve got the rights to, that you’d like to include on your page. Save a copy of it to the igme110 folder. 

You’re going to add code to your HTML to display the image properly on the page. In Komodo edit, put your cursor after the heading with your name, but before the first paragraph of text. (If there’s not a blank line there already, you can add one, to make the code easier to read.) Type in `<img src="" alt="">` (or, use the Emmet shortcut by typing `img` and pressing tab). 

Between the quote marks following src, you're going to add the *relative* path to the image you downloaded. Because the image is in the same directory as your html file, the relative path is just the file name--if you don’t provide any other information besides a file name, the browser will assume that the image is in the same directory as the HTML file it’s displaying. My image file is called dog.jpg, so my tag would now look like this:
```<img src="dog.jpg" alt="" />```

Between the quote marks following alt, you’re going to add text that will display if the browser is unable to display images. My tag now looks like this:
```<img src="dog.jpg" alt="Morgan the dog” />```

Save your file, go back to the browser window that you used to view it in the last section, and reload the file. It should now look something like this:

![index.html with image added](110homepage-2.png) 

Add a paragraph of text after the title, describing the image. Include information about where you got the image--including a link back to the source if it's not an image you took yourself.
 
If your image isn’t showing up properly, ask for help now! (If it’s much too big to display properly on the page, try finding and downloading a smaller image from the web. )

## Relative References to Other Directories

As your web site gets bigger, keeping all your files in the same directory makes it harder to keep them organized. Web developers typically have different directories for different parts of their site, and also often  keep images in a separate directory. You created a media folder in your www directory, and that’s where we’re going to put the images you use on your site. 

On your computer, open the igme110 folder you created. Move your image file from igme110 into the media folder. (Your structure should look like this:

![index.html with image added](110homepage-folderstructure.png) 

Now try reloading your page in the browser again.  If you followed the directions properly, the image won’t load now. The browser is still looking for it in the same directory as the HTML file, but it’s not there. We need to tell the browser how to find the image, using a relative path. 

In your html file, change the img tag so that it looks like this (using your image information, of course):
   ```<img src="media/dog.jpg" alt="Morgan the dog" />```

This tells the browser to look in the media folder that’s inside the igme110 folder. Reload the page in the browser to see if it worked. The image should show up again. (If not, ask for help!)

## Creating and Linking to a Second Page

Using your HTML editor, create a new HTML 5 file. Save it with the name page2.html. Give it a title of “Your Name’s Second Page.” (Put that in the title tag, as well as in a level 1 heading on the page.) 

Add an image to this page, as well, and a paragraph of text with whatever content you'd like. 

Add a second paragraph with a link back to your index.html page. Because we’re using relative links, and because the file is in the same igme110 directory, you only have to specify the file name, like this:
   ```<p><a href="index.html">My First Page</a></p>```

Go back to your index.html file, and add a link at the end of that page to your new HTML file, like this:
```<p><a href="page2.html">My Second Page</a></p>```

Here's an example:

![Screenshot of Example Page 2][110homepage-3.png]

In your web browser, reload your index.html page, and make sure the links between your pages work properly. If they don’t, ask for help! 

## Uploading

Now we’ll use FTP (actually SFTP, which uses a secure connection to the server) to put your web pages onto the banjo server.

Launch FileZilla.  Fill in the fields at the top with the following information, and click “Quickconnect”:
![FileZilla Connect Screen](filezilla-connect.png)

FileZilla may ask you if you want it to remember passwords—if you’re doing this in the lab, tell it no. If this is the first time you've used FileZilla on a lab computer, it may also give you a warning about an “unknown host key”—if that happens, check the box saying “Always trust this host” and then click OK. If you entered your user ID and password correctly, you should now see something like this:
![FileZilla File Listing Screen](filezilla-files.png)

The pane on the bottom left shows the files on your computer’s hard drive. In this case, it’s showing everything, including hidden files, that are on the main level of my computer’s hard drive. The pane on the right shows all the files in your directory on RIT’s web server. 

In the pane on the left side (local site files), you’ll need to find the directory that you created at the beginning of this exercise. If you put it on a thumb drive, the drive should show up in the Volumes directory. If you put it on the Desktop, it should be in the student directory inside of the Users directory. You want to find your www folder and open it, so that you can see the igme110 and media folders in the left pane. (If you’re using Mac, there may also be a hidden file called .DS_Store, which you can ignore—it’s a Mac system file that is hidden.) If you have trouble finding your files, ask for help. 

In the pane on the right side (server files), double click on the www directory. You should see the 110 directory that you created in Tuesday’s exercise. Leave that alone until you’ve gotten credit for the exercise! 

Once you’ve got the www directory on your local computer on the left side, and the www directory on banjo on the right side, you’re going to drag the igme110 directory from the www folder on the left (your computer) to the www folder on the right (the server). This will copy the folder and its contents to the web server. The file list on the right side should update to show the the new directories. 

Now you need to test the files on the web server, to see if they’re accessible. Use a browser to go to `http://people.rit.edu/youruserid/igme110` (substituting your RIT ID for *youruserid*)

If the files and images show up, great! But it’s possible that they won’t, because the access to the files may not be set properly by default. I’ll review how to change permissions on files in our class, but for reference purposes, here’s how to do it:

In FileZilla, right click on the folder in the right pane, choose “File Permissions” and make sure the permissions include read write and execute for the owner (that’s you), and read and execute for everyone else. The number in the box at the bottom should read “755” which is shorthand for those permissions. (You can either type the number into the box at the bottom, or check the boxes next to the permissions you want.) 
Once you’ve checked the permissions on the folders, you need to also check the permissions for the individual files. Double click on a folder to open it, and repeat the process of right-clicking and choosing File Permissions for each of the individual files. The HTML and image files don’t need execute permissions, so the shortcut for their permissions is 644 rather than 755. 

Once you’re sure all the files have the right permissions, go back to the browser and try loading the URL above one more time. If it still won't load, ask for help!

Notice that the URL I gave you only has the directory name (igme110) and not a file name. That is because banjo, like most web servers, automatically looks for a file called index.html in a folder if no other file was specified. If you were to include the file name in the URL (e.g. `http://people.rit.edu/youruserid/igme110/index.html`), it would also recognize that file and load it. But if you end the URL with the directory name and don’t specify a file, the server will automatically load the index.html file if there is one in that directory. 

Once your page has displayed properly, view the source in the web browser (if you're using Chrome, type Ctrl-U to display the page source). You'll probably see a big block of completely unfamiliar code near the top of your page, where your first image is embedded. In the next section, I'll explain where that came from, and how we can make it go away. 

## Fixing Banjo

banjo.rit.edu uses specific server-techniques to help pages across RIT's sites load faster, but these techniques have the side effect of making pages on the server harder for us to debug and to validate.

To fix this, you're going to need to copy a file from my www directory to yours via the command line. As you did on Tuesday, use PuTTY (or Terminal on a Mac) to connect to banjo.rit.edu, and then type the following commands:

```
cd www
cp ~ellics/www/.htaccess .htaccess
chmod 644 .htaccess
```

The first line changes directories into your www directory. The second line copies a file called .htaccess from my www directory to your www directory. And the third line changes the permissions on the .htaccess file so that the web server can read it. 

Go back to Chrome, reload your index.html page, and view the source again. If it all worked properly, the block of code inserted by the server that you saw before should now be gone. 

## Due Date
You must have this exercise complete by noon on Saturday, September 30th. On Saturday, my TA will check to see if you completed the work by loading  `http://people.rit.edu/youruserid/igme110` and making sure that the files are present and include the requested components. 