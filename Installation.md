# Angular2Trial in ubuntu 16 Xenial

<h3> uninstall exsisiting npm  </h3>
sudo apt-get remove nodejs </br>
sudo apt-get remove npm </br>
sudo apt-get update </br>

Check for any .npm or .node folder in your home folder and delete those.
If you type

which node </br>

sudo apt-get autoremove </br>
sudo apt-get autoclean  </br>


<h3> Install Using NVM </h3>

sudo apt-get update </br>
sudo apt-get install build-essential libssl-dev  </br>
curl -sL https://raw.githubusercontent.com/creationix/nvm/v0.31.0/install.sh -o install_nvm.sh </br>

And inspect the installation script with nano: </br>
nano install_nvm.sh   </br>

Run the script with bash:  </br>
bash install_nvm.sh  </br>
source ~/.profile  </br>

Now that you have nvm installed, you can install isolated Node.js versions.To find out the versions of Node.js that are     available for installation, you can type: </br>

nvm ls-remote

Output
...
         v5.8.0
         v5.9.0
         v5.9.1
        v5.10.0
        v5.10.1
        v5.11.0
         v6.0.0

As you can see, the newest version at the time of this writing is v6.0.0. You can install that by typing:
nvm install 6.0.0

Usually, nvm will switch to use the most recently installed version. You can explicitly tell nvm to use the version we just downloaded by typing:

    nvm use 6.0.0

When you install Node.js using nvm, the executable is called node. You can see the version currently being used by the shell by typing:

node -v

Output
v6.0.0

If you have multiple Node.js versions, you can see what is installed by typing:

nvm ls

If you wish to default one of the versions, you can type:

nvm alias default 6.0.0

This version will be automatically selected when a new session spawns. You can also reference it by the alias like this:

nvm use default

sudo npm install -g angular-cli


<h3> create new project </h3>
ng new first-app  </br>
ng serve

--> hit localhost:4200

<h4> Removing the following warning </h4>
warning :
Experimental support for decorators is a feature that is subject to change in a future release. Set the 'experimentalDecorators' option to remove this warning. class AppComponent

how to remove it :
Go to File > Preferences > Workspace Settings then add the below to settings.json

// Place your settings in this file to overwrite default and user settings.  </br>
{ "typescript.tsdk": "./node_modules/typescript/lib" }

Then go to View > Command Palette > type "reload window" in panel and press enter.
