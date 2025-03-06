### create react application

# enter following code on terminal
npm create vite@latest
# then enter Y
# then give project name
# then give package name
# then choose react framework
# then choose javascript variant, and project will be created

npm install

## changed preview in package.json file to run in local machine
earlier>>>   "preview": "vite build; vite preview --host"
now>>>>      "preview": "vite build && vite preview --host"

# run react project
npm run preview

# linking project with my github
git init

git config --global user.email "shehab10111995@gmail.com"
git config --global user.name "HASAN9519"
git add --a
git commit -m "initial commit"
git branch -M main

# linking project with created github repo
git remote add origin https://github.com/HASAN9519/sampleReactAppwithgithubdeployment.git
git push -u origin main