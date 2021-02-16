# Starter Boilerplate

A starter boilerplate, will help us not to repeat our self every time we have to work on a new practice or project, by creating the folders and files mentioned in dealing with files and folders. Since we will be creating the same folder and most likely the same files name, we can make a boilerplate, which we re-use for each of practice or project.

This boilerplate could grow to be a starting point for all your future projects, where by you will not repeat your self on common functionalities.

Now, lets create our starter boilerplate:

1. Open the **web-projects** folder you created earlier.
2. Inside the web-projects folder, create a new folder called **starter-boilerplate**
3. Open the **starter-boilerplate** folder via VS Code
4. Within VS Code let's create the following files and folders
   1. create a new file **index.html**
   2. create a new folder called **css** and within this css folder create a new file called **style.css**
   3. create a new folder called **js** and within this js folder create a new file called **script.js**
   4. create a new folder called **images**

If all goes well, your starter boilerplate should look like this

![Starter Boilerplate]()

## File paths

To make files talk to one another, you have to provide a file path  between them — basically a route, so one file knows where another one  is. 

To demonstrate this, we will populate our `index.html` file with the HTML document structure and do the following:

1. Open up your `index.html` file, and generate the HTML document structure.

2. Update the `title` content to **Starter Boilerplate**   

3. Within the `head` element, just before the closing `</head>` tag, insert a new element called `link`. This element will make our HTML and CSS talk to each other.

   Example:

   ```html
   <link rel="stylesheet" href="css/style.css">
   ```

4. Within the `body` element, just before the closing `</body>` tag, insert a new element called `script`. This element will make our HTML and JS talk to each other.

   Example:

   ```html
   <script src="./js/script.js"></script>
   ```

5. Do `Ctrl+S` to save the HTML file

For now, this is about all you need to know.

**Note**: Some general rules to adhere to for file paths

- To reference a file in the same folder as the invoking file (HTML, CSS or JS), just use the filename.
- To reference a file in a sub-folder, write the folder name in front of the path, plus a forward slash, then the file name.
- To reference a file in the folder above the invoking file (HTML, CSS or JS), write two dots in front of the path, plus a forward slash, the folder name or file name. 