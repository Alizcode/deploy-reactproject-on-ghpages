# Step 1:
***
- push your project at github as you normally do e.g
- make a new Repo- add>> commit>> push
- make sure your git repo name and project names are same.
# Step 2: 
open terminal & Install gh-pages module in React app
> npm install --save gh-pages

# Step 3:
Now make following changes in package.json file.
Add homepage url below name
> "homepage": "https://{GitHub-username}.github.io/{ProjectName}/" 

 `without braces of course`.
Add these lines inside scripts object

> "predeploy": "npm run build",
    "deploy": "gh-pages -d build",


After changes package.json file will look something like this.

{
  "name": "ghtest",
  "homepage": "https://{GH-username}.github.io/{projectName}/", 
  "version": "0.1.0",
  "private": true,
  "dependencies": {
    "gh-pages": "^2.2.0",
    "react": "^16.12.0",
    "react-dom": "^16.12.0",
    "react-scripts": "3.3.0"
  },
  "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test",
    "predeploy": "npm run build",
    "deploy": "gh-pages -d build",
    "eject": "react-scripts eject"
  }
}

# Last step 
Deploy using this command

> npm run deploy