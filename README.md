# first-electron-app
develop a simple desktop app with electron

# step1
Go to https://nodejs.org/en/ to download Node.js(v7.9.0 Current), and then install it.

# step2
Create a new directory for your app. Mine is E:\StudyNewTechnology\LearningElectron\first-electron-app, use cmd.exe to go to the directory you just created.
and type command npm init, this will walk you through creating a package.json file.

# step3
After you succeeded in creating the package.json file, please type command npm install electron, and then wait it to be installed. You probably will encounter node install.js failed problem.
Here's the solution, go to nodejs installed directory, mine is C:\Program Files\nodejs\node_modules\npm\, add this line electron_mirror="https://npm.taobao.org/mirrors/electron/" and then try again.
You'll probably succeed this time.

# step4
Go to package.json change the start property of scripts as "electron index.js"

create index.js file:
const electron = require('electron');
const {app,BrowserWindow} = electron;

app.on('ready', ()=>
{
    let win = new BrowserWindow({width:800,height:600});
    win.loadURL(`file://${__dirname}/index.html`);
})

create index.html file:
<!doc html>
<head>
<title>
wuxu's first electron app
</title>
</head>

<body>
<h1>this is my first Electron app!</h1>

</body>

</html>

# step 5
type command npm start, and you'll see the window!!!