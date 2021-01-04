# simple-website

This is a demo website.

* `index.html` contains the contents of the website
* `styles.css` contains the styles (background, colors, fonts, etc...)
* `main.js` contains the JavaScript code for the interactive elements of the site (clicking on the image to interact with it)

## Part 1: Fork This repository

This repository is currently stored within the `code4policy` account on GitHub. By creating a fork, you will be making a copy of it under your own GitHub account. The fork will retain a connection to the original repository, however it will be a full copy of the code and the entire Git history.

![](https://www.evernote.com/shard/s150/sh/b9e1620e-5f1d-4bac-9b89-df3b46007c13/6f42203c4318df0c/res/3666da39-069a-47a8-ad14-8db56c12ec17)

In this exercise, we're going to focus on developing code locally (on your computer) and pushing it up to the remote repository (your fork on GitHub).

## Part 2: Host Your Website

GitHub also doubles as a static web server! If you enable a feature called "[GitHub Pages](https://pages.github.com/)", in addition to storing your files, GitHub will run a static web server that can serve those pages on the web.

1. Go to this github repo's settings and under Github Pages choose "main" branch as the source. (screenshot shows "master" branch which is the old GitHub terminology for the "main" branch)

	![](https://i.imgur.com/8EhdwWM.png)

2. Go to the specified URL (it will likely be username.github.io/simple-website, where "username" is your GitHub username) and you should see the HTML page we created. You might have to wait a minute or two before it shows up.

## Part 3: Developing Locally (on your computer)

### Cloning The Repository (making a local copy on your computer)

1. Open your command line terminal and navigate to your Development folder
  
	```
	cd ~/Development/
	```

2. Clone the repository using the SSH link given to you in GitHub, it should look something like this:

	```
	git clone git@github.com:XXXXX/simple-website.git
	```

3. In the command line, navigate into that folder and then open it in your text editor. 

	```
	cd ~/Development/simple-website
	```

4. Now open the code in Sublime Text (or another text editor of your choice). Note, if the `subl .` command in the instructions below doesn't work for you, you can just open Sublime Text yourself and open this folder from within Sublime Text by clicking the "File" menu, then "Open".

	```
	subl ~/Development/simple-website
	```

4. Once you have the files on your computer, find them in and double click on `index.html` to view it in a web browser (you can refresh the page to view it again after you add new code). Congrats! You now have a copy of the website on your own computer. You'll notice the URL of your browser isn't on the web, now it is pointing to a file on your computer.

### Editing The Website

1. Lets create a new page called `goodbye.html`
	
2. Put the following code in `goodbye.html`. This is what a bare-bones HTML page looks like.

	```html
	<!DOCTYPE html>
	<html>

	  <head>
	    <title>Goodbye!</title>
	  </head>

	  <body>
	    <h1>Goodbye World</h1>
	    <h2>Adios</h2>
	    <p> What a short website </p>
	  </body>

	</html>
	```

3. Commit this page

	```
	git status
	git add goodbye.html
	git commit -m "add goodbye page"
	```

### Let's try that again by making another edit.

We're going to practice that workflow one more time. Lets add navigation.

1. In `index.html` inside the body tag, lets add the following.
	```
	<a href="goodbye.html"> Goodbye Page </a>
	```
	
	and in `goodbye.html` lets add a link back
	```
	<a href="index.html"> Home Page </a>
	```

2. Now if you refresh the page, or open `index.html` again in your browser, you should be able to navigate back and forth between the two pages!	

3. Once you see that the links are working correctly, lets commit both of those changes in one commit
	```
	git status
	git add index.html
	git add goodbye.html
	git commit -m "add navigation links to website"
	```

### Pushing to GitHub

1. Push to GitHub
	```
	git push
	```
  
	If this is the first time you're pushing, you may have to set an upstream branch. If you read the output of `git push` it will tell you what to do. Essentially this is just synchronizing this branch locally with the corresponding branch in the remote repository.

2. Once you've pushed the website to the main branch on GitHub, you should be able to view it online! Your URL will likely be something like: `username.github.io/simple-website`

### Final notes

Remmber, 

* you can always see what is in the **staging area** with `git status`
* you can always see what is in the **commit log** with `git log`

Use these commands frequently to build your mental model of what is going on in your Git repository.

### Part 4: Tasks

1. Make a change
2. Commit that change
3. Push to GitHub
4. Repeat 5 times

You can make any five changes you wish. At first, I'd reccomend simple changes, like updating text. Once you get the hang of it, you're welcome to update the styles, or edit the HTML. If you'd like to make more than 5 edits, feel free to keep going and have fun! I'd encourage you to keep going until you feel you've got the hang of how Git works.

More broadly, our goals with this assignment are to:

   1. build a mental model of the structure of the local Git repository (the one on your computer). What is in the staging area? What is in the commit log? Building and maintaining a mental model of what is going on is a key skill in working with code, even beyond GitHub.
   2. build some muscle memory around using Git from the command line, as we will be using these tools every day for the rest of the class

#### Bonus
Finally, if you'd like to pursue a third learning objective here, you may. That objective is to explore a new and unfamiliar codebase and understand how it works. See if you can figure out how to give every page in your website a consistent look and feel. To do this, you'll need to figure out how to link the same stylesheet to both `index.html` and `goodbye.html` as well as any other page you create. 

If you'd like to take a crack at playing around with the JavaScript...you may do that as well! Good luck!
    
   
