# mikeanddan.github.io

Repository for getmikeanddan.com

####Github Pages deployment process
Configuration based on example from [winstonyw](http://winstonyw.com/2013/02/24/jekyll_haml_sass_and_github_pages/). Adapted to use gh-pages branch, so that master can be preserved for primary development workflow.

##### Initial Configuration
From master:

1. `mkdir gh-pages`
2. `cd gh-pages`
3. `git init .`
4. `git commit -am "Initialize"`
5. `git remote add origin https://github.com/MikeAndDan/mikeanddan.git`
6. `cd ..`

Now you should be able to run `rake deploy` from master. WARNING: Be sure to always have a clean master branch when deploying. Running `rake deploy` on a branch with uncommitted changes WILL include those changes in the deploy.
