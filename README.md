# Rapid Prototyping : Write/Speak/Code Node.js Workshop

## Environment Setup

<strong>Please complete steps 1-4 before the workshop! It will let us get the most out of the time we have.</strong> 

<i>Disclaimer: I will be running the workshop on a Mac. I've linked resources below for Mac, Windows, and Linux, 
but I can't speak to how thorough the Windows/Linux resources are. Please seek out other resources if 
you run into trouble!</i>

1) Have a Text Editor or IDE ready. I will be doing the workshop in Visual Studio Code, but feel free to use your favorite editor. If you need to download one, I recommend Visual Studio Code (it's free):

	* Visual Studio Code: https://code.visualstudio.com/download

2) Install Node and npm. Instructions are for Mac, see Linux/Windows resources below. 

    <i>You'll need <strong>XCode</strong> and <strong>Homebrew</strong> before you install Node. Homebrew is a package manager for Mac OS that makes installing software easier. </i>

    Install Command Line Tools for XCode by opening Terminal and running:
    
        $ xcode-select --install

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

3. Set up git if you don't have it set up: https://help.github.com/articles/set-up-git/

4. Clone this repo!

	    $ git clone git@github.com:kelseyfrose/wsc-workshop.git

:tada: :tada: :tada: