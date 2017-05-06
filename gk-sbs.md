//001.CREATE PROJECT FOLDER
mkdir gk-sbs
cd gk-sbs

//Create a local git repo
echo "# GK-SBS" >> README.md
git init
git add README.md
git commit -m "Initial commit"

//Create a remote git repo
Create a project at github.com - https://github.com/htdong1980/gk-sbs.git
git remote add origin https://github.com/htdong1980/gk-sbs.git
git push -u origin master

//002.CREATE ANGULAR CLIENT
git clone https://github.com/htdong1980/quickstart.git client
cd client

//Remove unnecessary files
rm -rf .git
xargs rm -rf < non-essential-files.osx.txt
rm src/app/*.spec*.ts
rm non-essential-files.osx.txt

//Install
npm install

//Run
npm start - runs the compiler and a server at the same time, both in "watch mode".
npm run build - runs the TypeScript compiler once.
npm run build:w - runs the TypeScript compiler in watch mode; the process keeps running, awaiting changes to TypeScript files and re-compiling when it sees them.
npm run serve - runs the lite-server, a light-weight, static file server, written and maintained by John Papa and Christopher Martin with excellent support for Angular apps that use routing.

//Test
npm test - compiles, runs and watches the karma unit tests
npm run e2e - compiles and run protractor e2e tests, written in Typescript (*e2e-spec.ts)

//To exclude git
Edit file .git/info/exclude
.DS_Store
/client/node_modules/*
/client/src/app/*.spec*.ts
