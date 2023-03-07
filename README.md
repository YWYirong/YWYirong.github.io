# How to host your resume on Github Pages

How to host your resume on Github Pages with [Jekyll](https://jekyllrb.com/).

  

## Purpose

The purpose of the project is to show you step by step on how to use Github Pages with Jekyll to host our resume.

  

## Prerequisites

* Have a Github account

* A resume formatted in Markdown

* A text editor

  

## Instructions
Here is a quick overview when the project is finish:
![resume](https://github.com/YWYirong/YWYirong.github.io/blob/main/resume.gif)

### 1. Create a repository

Create a new repository on Github by clicking on the "+" icon in the upper right corner of the Github homepage and selecting "New Repository"name the repository *username.github.io*, replace username with your Github username.
```

The first part of repository name has to match your username, otherwise it won't work.

```
### 2. Clone the repository
If you are using terminal: go to the folder where you want your project to be stored, and then use 
```shell
git clone https://github.com/username/username.github.io
```
If you are using [Github Desktop](https://desktop.github.com/): Click the "set up in Desktop" button shown in the repository on Github website, then it will open Github Desktop, save the project.

### 3. Installing Jekyll
* About Jekyll: Jekyll is a tool for generating static websites that comes with integrated GitHub Pages support and a streamlined building process.

* Make sure you have [Ruby](https://www.ruby-lang.org/en/downloads/) and [RubyGems](https://rubygems.org/pages/download) installed beforehand.

To install Jekyll, using:
```shell
gem install jekyll
```

### 4. Create a new Jekyll site
1. Navigate to the publishing source for your site and create a new Jekyll site with:
	```shell
	jekyll new --skip-bundle .
	```
2. Open the Gemfile that Jekyll created. Comment out the line starts with "gem "jekyll" using "#".
3. Change the line with "gem "github-pages" into:
	```shell
	gem "github-pages", "~> GITHUB-PAGES-VERSION", group: 	:jekyll_plugins
	```
	Replace the "GITHUB-PAGES-VERSION" with current Github Pages version. To find the version see [here](https://pages.github.com/versions/).
4. From the command line, run `bundle install`
  

## More Resources

  
  

## Authors and Acknowledgments



  

## FAQs



