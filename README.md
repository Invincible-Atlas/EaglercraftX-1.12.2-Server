# EaglerCraftX Server Setup
## Introduction
Eaglercraft is an open-source web-based minecraft copy. Today I will teach you how to setup a public server with plugins for free! Please note that the project is an old one, and is not being actively maintained anymore. Because of this, you should consider hosting the server on a system outside of your network. Some examples include OCI and Github Codespaces. Now, lets begin! 

## Prerequisites
* A computer that can be running 24/7 (or can be started remotely)
    * Github codespaces will work, but you have limited hours and you have to interact with the codespace every 29 minutes otherwise it shuts down
* Said computer must have Java installed (if an error is thrown when you try to run the server, you got the wrong version. If this happens, only god or SuperUser can help you now)
* VSCode

## First-Time setup
### Clone the files
If you're using Github Codespaces, you can skip this step.
Use git clone to copy the files, or download the zip of this repo and unzip it.  
Open the folder in VSCode  
### Config and Setup
To configure your server, dick with the .yml and .properties files. I cannot help you further with this, it is an arcane art that can only be learned from experience.  
If you want to add a plugin, find a plugin for bukkit or spigot that works on 1.12.2, download it, and move the .jar to the ./server/plugins folder. I would recommend replacing the stock simplehomes and simpletpa with essentialsx, and loginsecurity with OpeNLogin. Make sure to delete the deleted plugins' folders *and* .jars. I would also recommend adding DisableMe, GriefPrevention, iControlU, Luckperms, and InvSeePlus.  
Remember, you can add plugins whenever you want, not just the first time you start the server. However, you have to shut down the server (with CTRL+C) and turn it back on for the changes to take effect.  
Then, run  `cd server && sudo java -jar server.jar`  
It will give you a EULA error. Go to the created eula.txt and change false to true.   

## Spin up the server
create 2 terminal tabs and paste in the following snippets:

first tab: `cd server && sudo java -jar server.jar`

second tab: `cd bungee && sudo java -jar bungee.jar`

## Making Server Public
Great! Now, you need to forward ports  `8081` and `25565` and navigate to your servers public ip [server-ip:8081]. The server welcome page should be displayed. Congrats on running your own server!

## Installing Plugins
In order to install plugins, navigate to `server > plugins`. You will need to clone the initial [plugin-name.jar] file as well as creating a separate directory in the plugins folder in order to store the additional data. Then just restart the server and the plugin should be running!
