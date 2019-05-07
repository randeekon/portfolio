Steps to reproduce

. go to terminal and to resume projects and create a folder called modern_portfolio using the command 

mkdir modern_portfolio

a new folder with that name is creatd in the resume projects folder ...then fo to that specific folder 

cd modern_portfolio

Now open visual studio from terminal by using the command:
 resume_projects\modern_portfolio\code .

the above command opens visual studio code with the respective folder directory.

In the visual studio add a few extensions like -- live server, prettier - code formatter, bracket pair colorizer
then u can save changes for format on save as enable true.

emmet will create code without writing when u want to create a html page then 
press 

! tab
this will create html structure
if u want to create a h1 then simply write h1 tab

now create a folder dist where all the html, css and js files will reside. create an index file woth the structure and write somethg in the body and open live server by right clicking.

now create another folder scss where all the scss files will be located, create a file main.scss in that folder which is the main scss file.

Node-sass

Node-sass is a library that provides binding for Node.js to LibSass, the C version of the popular stylesheet preprocessor, Sass.

It allows you to natively compile .scss files to css at incredible speed and automatically via a connect middleware.

Install
npm install node-sass

before installing node sass, install npm node modules - open terminal in Visual studio and 
npm init

then npm i node-sass

this command will create the required modules, dependencies etc
now open package.json file and make some changes to the key value pairs
"scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
change to the following

"scripts": {
    "sass": "node-sass -w scss/ -o dist/css/ --recursive "
  },

watch scss folder and output to dist/css flag recursive is to avoid issues with partials in reloads
save and run the command 
npm run sass
this will start the watch command 
now open scss/main.scss and write some basic code and save the file and run command
npm run sass this will automatically start the watch command and a new css file is compiled in the dist/css folder. css folder is created itself and a new file main.css is created and code is compiled from main.scss file to main.css file. u will get a green colr message int he terminal saying rendering complete.

u can check by opening the css file.
now include the css file link in the index.html page to render the changes

now open a new terminal and create a git repository. first create a file .gitignore using the command
touch .gitignore (touch creates a file named gitignore)
if u get error touch is not recognised as an internal or external command then run this command first:
npm install touch-cli -g
then touch .gitignore
now .gitignore file will be created it is an empty file ... u can write in it as node modules and save it run the command git init
this gives the message: initialized empty git repository
add all the files using the command 
git add .
git commit -m "initial workflow setup" //it works with " ", gives error with  ''
------------------------------------------------------
working on index home page

open visualstudio, run live server and open ur server
make menu in the nav
fontawesome.com and include the link in html page
<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.7.2/css/all.css" integrity="sha384-fnmOCqbTlWIlj8LyTjo7mOUStjsKC4pOpQbqyi7RrhN7udi9RwhKkMHpvLbHG9Sr" crossorigin="anonymous">

&.lg-heading is same as h1.lg-heading... we can do nesting in scss

font-size:6rem  rem is multipiler unit. 1 rem = 16px
default fontsize of html is 16px, so 6rem will be 16*6=96px. we can see in the developer tools also fontsize will be displayed as 96px.

20 vh (viewport height) like rem, vh is another unit of measurement.

after all the files are done 
add to git using git add .
git commit -m "____"
git push  and add origin commands
now after ur repo is created in git then to host ur website u can use pages.github.com
create another github repo randeekon.github.io and then follow the steps:
https://randeekon.github.io/portfolio/
https://randeekon.github.io/portfolio/index.html