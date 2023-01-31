# How to make a vue site and deploy publicly on github pages

# vue quick start:
# guide: https://vuejs.org/guide/quick-start.html#creating-a-vue-application
# check your node / npm versions.
# it will make the project inside a project folder,
# which will be your root, so you don't need to make a folder.
# Note: for github pages, if you're making your first one,
# name the project <USERNAME>.github.io,
# after your first one you can make them with any name,
# but you have to add a "project" to it to make pages.
# start a new vue app:
npm init vue@latest
# "no" to everything ok
# app is now created

# couple changes:
# if you're making <USERNAME>.github.io, your "base" is '/'.
# otherwise your base is the name of your git repository.
# add this under plugins in your vite.config.js file
base: '/<base>/',
# create vue.config.js and put this in:
// vue.config.js
module.exports = {
	publicPath: '/<base>/'
}

# see the site locally. and build:
npm install
npm run dev
# you can now see the dev site locally
npm run build
npm run preview
# you can now see the build locally

# git:
# create github repository with the same name as the project above
git init
# add anything you don't need into .gitignore, but don't ignore dist.
# push the first commit:
git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/<USER>/<REPO>
git push -u origin main
# see on github you pushed your source code
# set your github pages settings:
# source: deploy from a branch. branch: none, /root. for now.
# if first time, create gh-pages branch from main:
git checkout -b gh-pages main
# get just the dist folder from main into gh-pages branch, you need to know the commit code from main:
git checkout e0f7de754cc99c1caaa27ccbde973f2a9c27ecef dist
git add .
git commit -m "commit dist"
# if first push of gh-pages:
git push --set-upstream origin gh-pages
# otherwise just
git push
# go set the github pages settings to use the gh-pages branch
# that should deploy it. check in github actions to see deployment
