# Our First Site

[<- Go Back](internet.md)

Follow the next steps to create your first site!!

## Create a local site

1. Download & install [Visual Studio Code](https://code.visualstudio.com)
2. Create a folder with the name: `my-first-site`
![create site folder](resources/images/folder.png)
3. Open Visual Studio Code
![open Visual Studio Code](resources/images/open_folder.png)
4. Open my-first-site using Visual Studio Code
![open Visual Studio Code](resources/images/open_folder_2.png)
5. Create the following files inside the `my-first-site` folder :
  * index.html
  * styles.css
  * script.js
![open Visual Studio Code](resources/images/create_files.png)
6. Copy and Paste the following code on each document

### index.html
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <title>My First Site</title>
  <link rel="stylesheet" href="styles.css">
  <link rel="shortcut icon" href="favicon.ico" type="image/x-icon">
</head>
<body>
  <div>
    <h1>Hello World!!!</h1>
    <p>Now let's conquer the world!!</p>
    <button>Click Me</button>
  </div>
  <script src="script.js" type="text/javascript"></script>
</body>
</html>
```

### style.css
```css
body {
  background-color: lightgray;
  font-family: Arial;
  text-align: center;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 90vh;
  justify-content: center;
}

h1 {
  font-size: 72px;
}

p {
  font-size: 28px;
}

button {
    color: white;
    font-size: 125%;
    border-radius: 4px;
    border: none;
    text-shadow: 0 1px 1px rgba(0, 0, 0, 0.2);
    background: rgb(28, 184, 65);
    padding: 10px;
    outline: none;
    cursor: pointer;
}

button:hover {
  background: rgb(66, 184, 221);
  padding: 12px;
}
```

### script.js
```js
window.onload = function() {
  var button = document.querySelector('button');

  button.addEventListener('click', function() {
    alert("Let's Rock!!");
  });
}
```

7. Download the following [favicon.ico](resources/icons/favicon.ico) to my-first-site folder
8. Go to the `my-first-site` folder and double click the file `index.html`
9. You should see a web page like this one:
![My First Site](resources/images/my_first_site.png)

## Publish our Site

At this point we created our first web but we can only access it from our computer as it's running locally.
To be able to publish it we need a free hosting and a domain. For this we will use [GitHub Pages](https://pages.github.com/)

1. Open a browser and navigate to https://github.com/join.
2. Set up your account. Pick a username that is professional since employeers will look at this account. Click "Create an account". 
3. Choose your subscription. Choose **Free** and click "Continue".
4. (Optional) Tailor your experience. Fill out the details and click "Submit".
5. Verify email and log into your [GitHub Account](https://github.com/login).
6. Create a new repository called `my-first-site` and click "Create Repository".
7. Click the copy to keyboard the commands in "…or create a new repository on the command line" section. ![GitHub new repository](resources/images/first-site/github1.png)
8. In Visual Studio Code, open the [Integrated Terminal](https://code.visualstudio.com/docs/editor/integrated-terminal). ![Integrated Terminal](resources/images/first-site/terminal.png)
9. In the Integrated Terminal, paste the copied line from the "…or create a new repository on the command line" section. 
10. Login using your GitHub username and password.
    * If you are having issues using HTTPS, use SSH instead by [adding a new SSH key to your GitHub account](https://help.github.com/en/enterprise/2.15/user/articles/adding-a-new-ssh-key-to-your-github-account).
11. Go to the Version Control tab (in side navigation).
12. Click the "+" next to "Changes" to stage all changes. ![Visual Studio Code version control tab](resources/images/first-site/vs-code1.png)
13. At the top type "my first commit" into the bar and click the "✔". ![Visual Studio Code commiting changes](resources/images/first-site/vs-code2.png)
14. Click the "Syncronize Changes" button  and click "OK" to syncronize with GitHub. ![Visual Studio Code](resources/images/first-site/vs-code3.png)
15. Go to the repository page and refresh. You should see the files that you created. ![GitHub my-first-website repository](resources/images/first-site/github2.png)
16. Under your repository name, click "Settings". ![Repository settings button](https://help.github.com/assets/images/help/repository/repo-actions-settings.png)
17. Use the "Select" source drop-down menu to select "master branch" folder as your GitHub Pages publishing source. ![Select master as source](resources/images/first-site/github3.png)
18. Click the link in the GitHub pages section. ![Link where site is ready to published](resources/images/first-site/github4.png)
19. **Congratulations, you have your first site online!!**
![Congratulations](resources/images/congratulations.gif)

## Extra
* Change the h1 and p wording (index.html)
* Set the body background-color to red (style.css)
* Refresh the local site to see the changes
* Upload the changed files to deploy the new site version
* Try to create your own version of the site

## Resources
* [Create a GitHub account](https://github.com/join)
* [Create a repository](https://help.github.com/en/articles/create-a-repo)
* [Git Integration in Visual Studio Code](https://scotch.io/tutorials/git-integration-in-visual-studio-code)
* [Publish files using GitHub pages](https://help.github.com/en/articles/configuring-a-publishing-source-for-github-pages)
* [Favicon Generator](https://www.favicon-generator.org)
* [Getting started with Visual Studio Code - by John Papa](https://johnpapa.net/getting-started-with-visual-studio-code)

## Let's Git started
* [<- Internet](internet.md) - [Git & GitHub ->](git.md)