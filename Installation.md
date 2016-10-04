# Angular2Trial in ubuntu 16 Xenial

<h3> uninstall exsisiting npm  </h3>
sudo apt-get remove nodejs
sudo apt-get remove npm
sudo apt-get update

Check for any .npm or .node folder in your home folder and delete those.
If you type
which node

sudo apt-get autoremove
sudo apt-get autoclean


<h3> Install Using NVM </h3>
<p>
    sudo apt-get update
    sudo apt-get install build-essential libssl-dev
curl -sL https://raw.githubusercontent.com/creationix/nvm/v0.31.0/install.sh -o install_nvm.sh
And inspect the installation script with nano:
    nano install_nvm.sh
Run the script with bash:
    bash install_nvm.sh
    source ~/.profile

Now that you have nvm installed, you can install isolated Node.js versions.

To find out the versions of Node.js that are available for installation, you can type:

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
</p>

<h3> create new project </h3>
ng new first-app
ng serve

--> hit localhost:4200
