[![](https://img.shields.io/badge/Open%20In-RStudio%20Cloud-green)](https://rstudio.cloud/content/4771757) *Try without installing anything. Make sure to click the Make a Copy button or you will lose all your changes.*
 
# NOAA quarto simple website with R in qmd or Rmd files

This is a template for [a simple Quarto website](https://nmfs-opensci.github.io/NOAA-quarto-simple/) (`type: website`). It looks like a html book (`type: book`) but unlike the book type it only has html format and you will not have the download options. `type: website` is a common format for documentation. 

The repo includes a GitHub Action that will build the website automatically when you make changes to the files. The webpage will use the `gh-pages` branch. Serving the website files from this branch is a common way to keep all the website files from cluttering your main branch. 

**Warning:** Check that the settings will allow the GitHub Action to run. See the instructions below under "GitHub Set-up". Scroll down to the troubleshooting section if the website is not built by the GitHub Action.

**Note:** The GitHub Action installs R so you can render qmd files with R code. You will need to edit to install Python or Julia if your qmd uses those instead. If you have substantial computations, you don't want to be re-running all the computations for files that didn't change. Read about the [freeze option](https://quarto.org/docs/publishing/ci.html) for this situation. R users with complex reports with dependencies (so qmd B depends on qmd A or data file A) should be aware of the {targets} package which will help you keep track of files that need to be re-rendered due to changes in dependencies.

## GitHub Set-up

* Click the green "Use This Template" button to make a repository with this content. Make sure to make your repo public (since GitHub Pages doesn't work on private repos unless you have a paid account) and check box to include all the branches (so that you get the gh-pages branch).
<img width="637" alt="image" src="https://user-images.githubusercontent.com/2545978/197051535-c43c62de-17e8-40bf-a536-3eea8db250c4.png">

* Turn on GitHub Pages under Settings > Pages . You will set pages to be made from the gh-pages branch and root directory.
<img width="540" alt="image" src="https://user-images.githubusercontent.com/2545978/196808262-3d2262be-b9b5-4897-bba5-fc2f056dd335.png">

* Allow GitHub Actions under Settings > Actions > General
<img width="719" alt="image" src="https://user-images.githubusercontent.com/2545978/196808404-0c075fcf-db03-4516-88dd-3143b9fca475.png">

* Allow GitHub Actions to write to the gh-pages branch. Scroll to the bottom under Settings > Actions > General, and make sure "Read and Write" is selected.
<img width="658" alt="image" src="https://user-images.githubusercontent.com/2545978/214977476-d25721b9-a5a7-4128-adfc-ff76090b809a.png">

* Edit the repo description and Readme to add a link to the webpage. When you edit the description, you will see the link url in the url box or you can click on the Actions tab or the  Settings > Pages page to find the url to the Quarto website

## Customize

* Edit the qmd or md files in the `content` folder. qmd files can include code (R, Python, Julia) and lots of Quarto markdown bells and whistles (like call-outs, cross-references, auto-citations and much more).
* Add the files to `_quarto.yml`

## Troubleshooting builds

The most common trouble users run into is that the book is not rendering. Check the following:

* The `gh-pages` branch does not exist. If you forgot to check the check box to include all the branches when you created the repo from the template then it won't exist. The Action will fail if the gh-pages branch does not already exist. You can create the branch and then push a change to main to trigger the Action to run again.
* The GitHub Pages has not been set. You need to go to Pages under settings, and set Pages to build from the `gh-pages` branch.
* You did not allow GitHub Actions to run and/or did not give read/write permission. Go to Settings > Actions > General, and make sure Actions are allowed (top section) and they have read/write permission (bottom section).
* You did not push a change to the main branch. The Action is triggered by a push to main, so try making an edit to README.md and pushing that change.

<hr>

### Disclaimer

This repository is a scientific product and is not official communication of the National Oceanic and Atmospheric Administration, or the United States Department of Commerce. All NOAA GitHub project content is provided on an ‘as is’ basis and the user assumes responsibility for its use. Any claims against the Department of Commerce or Department of Commerce bureaus stemming from the use of this GitHub project will be governed by all applicable Federal law. Any reference to specific commercial products, processes, or services by service mark, trademark, manufacturer, or otherwise, does not constitute or imply their endorsement, recommendation or favoring by the Department of Commerce. The Department of Commerce seal and logo, or the seal and logo of a DOC bureau, shall not be used in any manner to imply endorsement of any commercial product or activity by DOC or the United States Government.

### License

This content was created by U.S. Government employees as part of their official duties. This content is not subject to copyright in the United States (17 U.S.C. §105) and is in the public domain within the United States of America. Additionally, copyright is waived worldwide through the CC0 1.0 Universal public domain dedication.

<hr>
