# Rapid Prototyping : Write/Speak/Code Node.js Workshop
[Environment Setup](#environment-setup)

[Workshop](#workshop) <br>
	1. [Hello World](#hello-world) <br>
	2. [API Integration](#api-integration) <br>
	3. [Project Structure](#project-structure) <br>
	4. [Adding a Front End](#adding-a-front-end)<br>
	5. [More Resources](#more-resources) <br>
	

## Environment Setup

<strong>Please complete steps 1-5 before the workshop! It will let us get the most out of the time we have.</strong> 

<i>Disclaimer: I will be running the workshop on a Mac. I've linked resources below for Mac, Windows, and Linux, 
but I can't speak to how thorough the Windows/Linux resources are. Please seek out other resources if 
you run into trouble!</i>

1) <strong> Have a Text Editor or IDE ready. </strong> I will be doing the workshop in Visual Studio Code, but feel free to use your favorite editor. If you need to download one, I recommend Visual Studio Code (it's free): 

	* Visual Studio Code: https://code.visualstudio.com/download

2) <strong> Install Node and npm. </strong> Instructions are for Mac, see Linux/Windows resources below.

    <i>You'll need <strong>XCode</strong> and <strong>Homebrew</strong> before you install Node. Homebrew is a package manager for Mac OS that makes installing software easier. </i>

    Install Command Line Tools for XCode by opening Terminal and running:
    
        $ xcode-select --install
    
    Don't worry if it prints `error: command line tools are already installed...`. You're good to go. 

    Then, check if you have Homebrew installed:

        $ brew -v
        
    If it isn't installed, your console will print `-bash: brew: command not found`. Install Homebrew with this command (more info here https://docs.brew.sh/Installation):

        $ mkdir homebrew && curl -L https://github.com/Homebrew/brew/tarball/master | tar xz --strip 1 -C homebrew

    Next, install Node
        
        $ brew install node

    Now you should have Node! To check: 

        $ node -v

    This should print a version number, like `v8.9.1`. 
        
    If you verified Node is installed, you're done with this step! For more information, or for Linux/Windows, check out the guides below for installing Node/npm

	* Mac: http://blog.teamtreehouse.com/install-node-js-npm-mac 
	* Linux: https://www.ostechnix.com/install-node-js-linux/
	* Windows: http://blog.teamtreehouse.com/install-node-js-npm-windows

3. <strong> Set up git if you don't have it set up </strong>: https://help.github.com/articles/set-up-git/

4. <strong> Clone this repo! </strong>

	    $ git clone git@github.com:kelseyfrose/wsc-workshop.git

5. <strong> Create or Login to a Foursquare account in order to get API keys. </strong>

    We'll be using Foursquare's API in this workshop. To get API keys, you'll need a Foursquare account- there's no separate Developer account, so a regular Foursquare account will do. After logging in, go to:

        https://foursquare.com/developers/apps

    to add a new app, which will generate your keys. For the app url, you can put `localhost:8000`

    IMPORTANT: <strong> You do not have to give credit card details to use the free plan! </strong> While adding an app to your developer account, you will see a prompt for credit card details. Scroll to the bottom and decline. You'll see your keys on the next page.


#### If you were able to complete all of the steps, you're totally ready to dive right in to the workshop! Thank you!!

#### If you ran into issues, we'll have some time at the beginning to catch you up, but you can also follow along without running the code on your machine.

:tada: :tada: :tada:



# Workshop 

## Hello World

#### npm install

After following the Environment Setup steps and cloning this repo, from inside the project directory, run 

    $ npm install

We're using npm, a package manager for Javascript. This command will install all of the dependencies defined inside `package.json`. You can see the installed dependencies inside `node_modules`. 

Next, we'll add a new dependency with npm:

    $ npm install lodash --save

Lodash is a popular utility Javascript package. Now, open package.json or run 

    $ cat package.json

to see that lodash is listed under `dependencies`. 

#### Demo - Using Express

To run the app from inside the project directory:

    $ node index.js

If you get `Error: listen EADDRINUSE :::8000`, you have a process running on that port already. You can change the port number from index.js (try 3000), or kill the process running on 8000.

After running `node index.js`, go to localhost:8000. You should see 'hello world!' in the browser window. Congrats! You have a Node app running.

Control-C in the command line will stop the node process and kill your server. 

#### Automatic Server Restarts

  Constantly stopping and restarting your server for small changes can get annoying. For automatic server restarts, you can install nodemon: 
  
    $ npm install -g nodemon
  
   The `-g` command means global. Adding `-g`  installs the package in your global `node_modules` . This means you can use nodemon in any directory, and it won’t be added to your project dependencies. 
  
  Running nodemon will restart your server automatically every time you make a file change. To run nodemon:
  
    $ nodemon index.js


## API Integration

To get your API keys, go to https://foursquare.com/developers/app/

We'll be using this API endpoint: https://developer.foursquare.com/docs/api/venues/search

Code from this section of the demo is [here](https://github.com/kelseyfrose/restaurant-roulette/tree/959841e3ea6f413e75d67639e7daa2b8345fa9e3)

## Project Structure

Code from this section of the demo is [here](https://github.com/kelseyfrose/restaurant-roulette/tree/50a3ef65b3f31a4834f3dddee7ccf1791a8dffdc)

## Adding a Front End

Code from this section of the demo is [here](https://github.com/kelseyfrose/restaurant-roulette/tree/4ce3fef114694903d83c15f5241b3d933455455e)

## More Resources

localtunnel and ngrok:

[localtunnel](https://localtunnel.github.io/www/) <br>
[ngrok](https://ngrok.com/download) <br>

Lightweight Databases - sqlite and NeDB

[sqlite](https://www.sqlite.org/index.html) <br>
[NeDB](https://www.npmjs.com/package/nedb) <br>




