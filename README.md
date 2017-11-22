
# Pre-Requirements
Current solution tested on Windows 7 x64 Maximum (with [babun shell](http://babun.github.io/)), but it also may run on OSX, Linux. Application is hard dependend on text extracting library [textract](https://github.com/dbashford/textract).

# Fast install

Project is nodejs cli application with some dependencies. If you already have installed copy of nodejs, you can just clone this repo and run `npm install`:

	git clone [Http link]
	npm install
	
# Step-by-step fresh installation

 - First, go to [nodejs](http://nodejs.org/) site, download and setup it for you platform
 - Then, clone this repo.
 - Run `npm install` in terminal from root folder of project to setup dependencies
 - At this moment application will work fine, but! By default it supports only `.TXT` and `.HTML` text formats. For better performance you should install at least support of `.PDF` (and `.DOC`). Here is instructions, how to do it from [textract README](https://github.com/dbashford/textract#requirements) file:
	 - `PDF` extraction requires `pdftotext` be installed, [link](http://www.foolabs.com/xpdf/download.html)
	 - `DOC` extraction requires `catdoc` be installed, [link](http://www.wagner.pp.ru/~vitus/software/catdoc/), unless on OSX in which case textutil (installed by default) is used.
	 - `DOCX` extraction requires `unzip` be available (e.g. `sudo apt-get install unzip` for Ubuntu)
		
> Please, note, that it's not necessary install support of all formats but preferably. As for me, I didn't get setup `catdoc` for `.DOC` files under Windows 7, so I played only with `.TXT`, `.HTML`, `.PDF` formats, but I know, it will also work with the rest formats :)

# Run

When you finish installation it's time to run application. Just put some Resume files to `/public` (it already has 3 for tests) directory and run in terminal `node app.js` from project's root. Then you can access JSONed results in `/compiled` folder (all file there will represent JSON string of parsed data.

Execution presents as dialog between `HR manager`, that has a lot of Resume to work with, and `BETSOL Parse Machine`, who volunteered to help with it, i thought that it should have some fun. 


# Technologies / References
Application built on javascript with [nodejs 0.10.31](http://nodejs.org/) under Windows 7 x64

Dependencies are:
- [cheerio](https://github.com/cheeriojs/cheerio)
- [colors](https://github.com/Marak/colors.js)
- [mime](https://github.com/broofa/node-mime)
- [request](https://github.com/request/request)
- [textract](https://github.com/dbashford/textract)
- [underscore](https://github.com/jashkenas/underscore)
    
# In action
![In action](/docs/result.png?raw=true "In action")