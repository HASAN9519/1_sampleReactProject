# create react application

### main instruction link

https://www.coursera.org/learn/developing-frontend-apps-with-react/ungradedLti/IXI0I/lab-setting-up-the-github-environment

https://author-ide.skills.network/render?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJtZF9pbnN0cnVjdGlvbnNfdXJsIjoiaHR0cHM6Ly9jZi1jb3Vyc2VzLWRhdGEuczMudXMuY2xvdWQtb2JqZWN0LXN0b3JhZ2UuYXBwZG9tYWluLmNsb3VkL0lCTVNraWxsc05ldHdvcmstQ0QwMjEwRU4tQ291cnNlcmEvbGFicy92Mi9tMS9TZXR0aW5nX3VwX3RoZV9lbnZpcm9ubWVudC5tZCIsInRvb2xfdHlwZSI6InRoZWlhIiwiYXRsYXNfZmlsZV9pZCI6NDIxMDQsImFkbWluIjpmYWxzZSwiaWF0IjoxNzMwMjIxNDgzfQ.NbUhkdxyb5ZCH0n1E-_Zq1FMDV7j2RPS5koHXoG_LhQ


### enter following code on terminal
npm create vite@latest
#### then enter Y, then give project name, then give package name, then choose react framework, then choose javascript variant, and project will be created

npm install

### changed preview in package.json file to run in local machine
earlier>>>   "preview": "vite build; vite preview --host"

now>>>>      "preview": "vite build && vite preview --host"

### run react project
npm run preview

### linking project with my github
### first create github repo without readme file
git init

git config --global user.email "shehab10111995@gmail.com"

git config --global user.name "HASAN9519"

git add --a

git commit -m "initial commit"

git branch -M main

### linking project with created github repo 
git remote add origin https://github.com/HASAN9519/1_sampleReactProject.git

git push -u origin main


### Deploy using GitHub Pages

#### To deploy your react application in GitHub you need to install gh-pages
npm install gh-pages --save-dev

#### Add given lines before "build": "vite build" in package.json file
"predeploy": "npm run build",
"deploy": "gh-pages -d dist",

#### in the vite.config.js file add this line before plugins: [react()]
base: "/REPOSITORY_NAME",

#### perform deploy command in the terminal to executes the "deploy" script defined in the package.json file, deploying the project to GitHub Pages using the gh-pages tool

npm run deploy
