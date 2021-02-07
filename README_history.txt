  # hannahpatellis video about github usage
  #
  # https://yul.cdn.nv.instructuremedia.com/originals/o-3dyWaoHDP987iHdMVs5qCcGoh11B95nL/transcodings/t-3ioziWMJLoXq1NJC9QXYV3T8dwc8uawu.mp4?&Expires=1612445097&Signature=njlRg0vOsjbkA~GHBD35yOWrMvaEGd73H4XYQatnfoj-eiBtXspesGIFH-FgyQLWe79JtyQ~tRiIVNbfzA-MO3vkNbXghqCurmCSwooDda5DHm9Ehls5x-ZE5G2iwbniZdrcnSLqTcwjIEeDxtU5i6yyOrwocj97pEr~VRRgI-djNYioL3ZYhW9B5q-wtwQBH85vdvVdTarmA2S3FARniE7Q~se00ISCeDSjfFHUw7gqHVTkbVfAHBHlL5OYBVQORTWYCUYN3i26AIEDCh7Y3X6IDTsfxI1S9ffh2vLNvVfjBlToCjZ1Em6l-Hm1wnYMvZXRVvLWfj3e3QgTeDV2hA__&Key-Pair-Id=APKAJLP4NHW7VFATZNDQ

  % pushd ~/Documents/UT_data_analytics/

  # login to my github accout
  # from the '+' pulldown menu in upper right, select "New repository"
  # use 'codingdemo' as the repo name
  # select 'initialize this repository with a README' checkbox
  # click 'Create repository'
  # click 'Clone or download' pulldown and select method (https, ssh, etc.)
  # copy command to clipboard, then on local host...

  % mkdir git
  % cd git

  # ssh version of clone won't work until I set up ssh keys (fix later)
  #git clone git@github.com:jilek/codingdemo.git

  # everything after 'clone' is pasted from clipboard (from github web page)
  % git clone https://github.com/jilek/codingdemo.git

  # narrator copies codingdemo folder in explorer onto vscode icon to open it
  % explorer .
  
  # use vscode code to create and save new file index.html

  # now stage, commit, and push from local host...

  # clone command creates new dir with name of repo
  % cd codingdemo/

  # stage changes to git repo (add 'A'll changes to staging area)
  % git add -A

  # commit with a 'm'essage 
  % git commit -m "Added an index.html file"

  # push changes to repo (old 'master' keyword is non-PC, now use 'main' branch)
  % git push origin main

  # now index.html and commit message show up on github web page

  # create a new 'b'ranch called "header"
  % git checkout -b header

  # edit index.html to add a new <h1> header

  # stage, commit, and push to new branch called "header"
  % git add -A
  % git commit -m "Added a header to index.html"
  % get push origin header

  # note that github page does not have new "Added a header..." message
  # that's because we are still on the main (old term master) branch
  # click the "Branch: main" pulldown and select "header" branch
  # note new commit message - yay!

  # create a "pull request"
  # on git page, note the yellow comment about change to 'header' branch
  # and green button to "Compare & pull request"
  # add a comment on "Open a pull request" page & click "Create pull request"
  # since no conflicts, click "Merge pull request" (no wait for approval)
  # click "Confirm merge"
  # Note purple icon & "Pull request successfully merged and closed" message
  # click "Delete branch" since we don't need it any more

  # switch to master branch on local host
  % git checkout master

  # note in vscode (or less) that <h1> header went away from index.html
  % less index.html 

  # pull any changes that have happened to master branch to local host
  % git pull

  # note change merged from "header" branch are now in "main" branch too
  # i.e. <h1> header is now in index.html file on main branch - yay!

