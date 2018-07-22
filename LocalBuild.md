### Steps for build site locally:
+ Push the current jekyll branch from local repo to master branch in GitHub: git push current_branch:master. This will create a master branch in Github repo
+ Make a copy of current repo and place it in a new folder, call it something like Static_Site
+ Delete everything from this folder except .git and .gitignore files
+ Now build the current working repo with github url instead of local host, this will repace all the localhost url with github page url, do the following: bundle exec jekyll build site.url
+ Step above will read the site url from _config
+ Now copy all the contents under _site folder within the currently working folder
+ Place them inside Static_Site
+ Create a file call .nojekyll within this folder
+ Add all files to git: git add .
+ Commit the changes
+ Push to the gh-pages: git push origin gh-pages -f. This will force update the gh-pages on Github
