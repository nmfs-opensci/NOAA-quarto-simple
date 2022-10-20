[![](https://img.shields.io/badge/Open%20In-RStudio%20Cloud-green)](https://rstudio.cloud/content/4771757) *Try without installing anything. Make sure to make click the Make a Copy button or you will lose all your changes.*
 
# NOAA quarto simple website

This is a template for [a simple Quarto website](https://nmfs-opensci.github.io/NOAA-quarto-simple/) that looks like a "book". This is a common format for documentation. It includes a GitHub Action that will build the website automatically when you make changes to the files. The webpage will use the `gh-pages` branch. Serving the website files from this branch is a common way to keep all the website files from cluttering your main branch. 

## GitHub Set-up

* Click the green "Use This Template" button to make a repository with this content. Make sure to make your repo public (since GitHub Pages doesn't work on private repos unless you have a paid account) and check box to include all the branches (so that you get the gh-pages branch).
<img width="637" alt="image" src="https://user-images.githubusercontent.com/2545978/197051535-c43c62de-17e8-40bf-a536-3eea8db250c4.png">

* Turn on GitHub Pages under Settings > Pages . You will set pages to be made from the gh-pages branch and root directory.
<img width="540" alt="image" src="https://user-images.githubusercontent.com/2545978/196808262-3d2262be-b9b5-4897-bba5-fc2f056dd335.png">

* Turn on GitHub Actions under Settings > Actions > General
<img width="719" alt="image" src="https://user-images.githubusercontent.com/2545978/196808404-0c075fcf-db03-4516-88dd-3143b9fca475.png">

* Edit the repo description and Readme to add a link to the webpage. When you edit the description, you will see the link url in the url box or you can click on the Actions tab or the  Settings > Pages page to find the url to the Quarto website

## Customize

* Edit the qmd or md files in the `content` folder. qmd files can include code (R, Python, Julia) and lots of Quarto markdown bells and whistles (like call-outs, cross-references, auto-citations and much more).
* Add the files to `_quarto.yml`

