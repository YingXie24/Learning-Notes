## How to install R
1.Go to Cran homepage at cran.r-project.org
1. Click on the base link
1. Click on the link at the top of the page that says "Download R version number for Windows"
1. Follow the setup intructions that follow. Default settings are fine.

## How to install Rstudio
1. Go to Rstudio download homepage
1. Click on RStudio Desktop (free)
1. Download the appropriate version for your laptop

## Configuring RStudio
1. Set up 4 quadrants: Source (top left), console (bottom left), environment (top right), Files (bottom right)
  - If you are missing the Source quadrant, go to File > New File > R Script
1. In files tab at the bottom right quadrant, set up working directory by clicking on the three dots on the far right. Then click on the "More" cogwheel and click "Set as working directory"

## Exploring R Studio
### Menu bar
1. File menu lets you create new files and Projects
2. Session menu lets you restart, interrupt or terminate R
3. Tools menu lets you install new packages, set up version control, set personal preferences for looks and functions


### Explaining the various quadrants:
1. console-- where our code is input and run
2. environment -- it lists all objects that had been created within an R session and allows you to view these objects in a new tab and source . There is a history tab that keeps a record of all commands that have been run. It also presents the option to either rerun the command in the console or send the command to source to be saved
3. Source -- where you save your R commands
4. Bottom right quadrant -- Files tab contains a listing of all the files in your working directory. Plots tab displays generated plots. Packages tab lists installed packages. Hep tab supplies help files for your R packages and various functions- in the upper right of this panel there is a search function.

## R packages
### The big three R repositories to find R packages
- CRAN
- Bioconductor
- Github

### Choosing the right package
- Cran has a Task view which categorises all packages into 35 themes
- Go to R documentation website, which is a search engine for packages and functions from CRAN, Bioconductor, and Github, that is, the big three R repositories. It also has a Task view that allows you to browse themes

### How to install packages
1. To install from the CRAN repository, type in console: install.packages("package_name"); or install.packages(c("package_name1, package_name2"). Alternatively, click Tools menu > Install Packages...
2. To install from Bioconductor, type source("https://bioconductor.org/biocLite.R") . Then, type biocLite("package_name")
3. To download from Github, install.packages("devtools"). Then library(devtools). Then install_github("author/package_name")

Once the package is downloaded, you need to **load** the package to R to make it available. To do so, type library(package_name). No quotation marks!
Alternatively go to bottom right quadrant > packages tab > tick the box

### Updating, removing, unloading packages
1. To check if a package is installed: installed.packages() or library(). Alternatively the Packages tab will show.
2. To check which packages need an update: old.packages()
1. To update all packages: update.packages(). To update a specific package: install.packages('package_name'). Alternatively go to the bottom right Packages tab and click Update tab
1. To unload a package: detach("package:package_name", unload = TRUE). Alternatively untick package in the Packages tab
1. To uninstall package: remove.packages("package_name"). Alternatively click on the cross icon behind the Package name in the GUI.
1. To check R version, type version.
1. Another helpful command for version of R and listing of all packages loaded, type sessionInfo(). This output of this command is a great detail to include when posing a question to forums- it tells a lot of info about your OS, R and the packages that you are using.

### Using the commands in a function
1. To check functions available in a package: help(package = "package_name"). Alternatively in GUI> Package tab> Click on the package
1. For more detailed explanation of what the package is and what each function is for: browseVignettes("package_name")

## Projects in R
Creating a project in R will create a new folder and assign that as the working directory so that all files generated will be assigned to the same directory. When you reopen a project, RStudio remembers what files were open and will restore the work environment- which is very helpful when you are starting back up on a project after some time off!

### Creating a project from scratch
1. Click File> New Project > New Directory > New Project. This creates a file in Files tab with .Rproj  
1. To open project, just open as normal in computer. Alternatively in RStudio, go to File> Open Project
1. To quit project, File > Close Project. Or just close RStudio window
1. To open several projects at the same time, File> Open Project in New Session

### Best practices
1. For organisation, in your projects folder (not the .Rproj file!), create folders Data, Scripts and Output.

## Project under Version Control
### Configurations
1. Get a github account
2. Install Git on your computer
3. Configure Git. Type: git config --list and check user.name and user.email
4. Type: git config --global user.name "YourUserName" to change user name
5. Type: git config --global user.email "YourEmail" to change email. **Make sure to use the same email address you signed up for GitHub with!**

### Linking Git and RStudio
1. In RStudio, go to Tools> Global Options> Git/SVN
1. Confirm that git.exe resides in the directory that RStudio has specified. Click Ok or Apply. RStudio and Git are now linked.

### Linking GitHub and RStudio
1. In the same Option window, click "Create RSA Key" and when this completes, click "Close".
1. In the same window, click "View public key" and copy the string. Close the window.
1. Go to github.com, go to account settings. Go to "SSH and GPG keys" > "New SSH Key". Paste in the public key and give it a title related to RStudio

### Create a new repository and edit it in RStudio
1. Create GitHub repository
1. In RStudio, go to File, New Project, Version Control
1. Select Git as your version control system
1. Provide the URL of the GitHub repository that you are attempting to clone (or just your own Github repository) and select a location on your computer to store the files locally
1. Click Create Project
1. In the environment quadrant, under Git tab, click the Checkbox under "Staged". Click "Commit". In the "Commit mesage" box, write a commit message. Click "Commit". Click "Push" on top right to commit to GitHub repository

### Collaborating with other's repository
1.Same as above, but using URL of the team's repository

### Linking an existing R project to Version control
1. Go to File, New Project, New Directory, New Project. Name your project. Do not click Create a git repository, click Create Project.
1. Open Git Bash in the directory containing your project files.
1. Type git init > Type git add . > Type git commit -m "initial commit"
1. To link to GitHub, go to github.com. Create a new repository. Make sure the name is the exact same as your R project and do not initialize the readme file, gitignore or licence.
1. Under the option to push an existing repo from the command line, copy the lines of code and paste it in your GitBash Terminal

## R Markdown
R Markdown is a way of creating fully reproducible documents, in which both text and code can be combined. Despite these documents all starting as plain text, you can render them into HTML pages, PDFs or Word documents, or slides! Also, it works very well with version control systems.

## Installation
Install R packages by typing install.packages("rmarkdown")

### Getting started with R Markdown
1. To create an R Markdown document, go to File > New File > R Markdown. Fill in the tile and an author and choose the output format
2. To create the final document, click on the "Knit" button along the top of the source panel
