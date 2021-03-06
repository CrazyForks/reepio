reep.io
=======
A browser based peer-to-peer file transfer platform. It is running at [https://reep.io](https://reep.io)

What is reep.io?
---
reep.io uses WebRTC technology to enable peer-to-peer file transfers between two browser without any server interaction. 
This repository holds the sources to run the reep.io frontend.  
**You will need a ICE and Peering server to run this project.** You can find the reep.io peering server [here](https://github.com/KodeKraftwerk/reepio-peering-server)

Configuration
---
You can set some options in the public/config.js (if it does not exist, copy the config.dist.js)
Have a look into the `config.dist.js` to get an overview over the available options

Running locally
---
	cp public/config.dist.js public/config.js
	npm install
	npm run build
	npm start

The build script is run every time something has changed inside the `src` folder.

You can now access the site by visiting [http://127.0.0.1:9001/]()

Running with Vagrant
---
	vagrant up
	vagrant ssh 
	cd reepio
	cp public/config.dist.js public/config.js
	npm install
	npm run build
	npm start

You can now access the site by visiting [http://192.168.0.120:9001/]()

Running Unit-Tests
---
You will have to run the end-to-end unit tests on your local machine, as the vagrant box has no gui or browser binaries.

To do so, just run the following command:

	npm test


License
---
reep.io uses the [GPL v2](http://www.gnu.org/licenses/gpl-2.0.html) license  
