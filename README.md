# How to host your resume on GitHub Pages

How to host your resume on GitHub Pages with [Jekyll](https://jekyllrb.com/).

## Purpose

The project aims to show you step-by-step how to use Github Pages with Jekyll (static site generator) to host our resume. As mentioned in the [Modern Technical Writing](https://www.amazon.ca/Modern-Technical-Writing-Introduction-Documentation-ebook/dp/B01A2QL9SS), a static site is fast, simple, portable, and secure, thus a great way to host your resume.

  
## Prerequisites

* Have a GitHub account

* A resume formatted in Markdown

* A text editor

  

## Instructions
Here is a quick overview of when the project is finished:
![](https://github.com/YWYirong/YWYirong.github.io/blob/main/resume.gif)

### 1. Create a repository

1. Create a new repository on Github by clicking on the "+" icon in the upper right corner of the Github homepage and selecting "New Repository". 

2. Name the repository *username.github.io*, and replace the username with your Github username.
```

The first part of repository name has to match your username, otherwise it won't work.
```

### 2. Clone the repository
* If you are using terminal: go to the folder where you want your project to be stored, and then use 
	```shell
	git clone https://github.com/username/username.github.io
	```
* If you are using [GitHub Desktop](https://desktop.github.com/): Click the "set up in Desktop" button shown in the repository on GitHub website, then it will open GitHub Desktop, and save the project.

### 3. Install Jekyll
* About Jekyll: Jekyll is a tool for generating static websites that come with integrated GitHub Pages support and a streamlined building process.

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
	Replace the "GITHUB-PAGES-VERSION" with the current GitHub Pages version. To find the version see [here](https://pages.github.com/versions/).

4. From the command line, run `bundle install`

5. Commit and push your work, don't forget to do this every time there are changes in your project.
	* Optionally, if you want to see how your website looks locally, run `shell bundle exec jekyll serve`.
	* Find the line start with"
Server address: http://127.0.0.1:4000/".
	* Navigate to the address shown in your terminal and see what your website looks like from local.


### 5. Add a theme to your website
1. Navigate to your site's repository.

2. Navigate to  *_config.yml*.

3.  Add `theme: THEME-NAME`, and replace THEME-NAME with a theme that GitHub support, see the [Supported theme](https://pages.github.com/themes/).

4. Optionally, to use any other Jekyll theme, use `remote_theme: THEME-NAME`, and change the THEME-NAME to the theme name shown in the readme file for that theme's repository.


### 6. Add your theme's CSS
1. Nagivate to the theme's repository and copy the *_/assets/css/style.scss_* file, or follow their instruction on how to set the CSS style. 

2. Navigate to the publishing source for your site.

3. Create a file name "*_/assets/css/style.scss_*", and copy the content provided from the theme repository.

### 7. Add the resume on your website
* Navigate to the publishing source for your site.

* if you want to host the resume as a post:
	1. Located the "*_posts*" folder.

	2.  Create a new file called  *YYYY-MM-DD-NAME-OF-POST.md*, replacing  *YYYY-MM-DD*  with the date of your post and  *NAME-OF-POST*  with the name of your post.

	3. Add the following YAML frontmatter to the file, where the layout should be a preferred style from the theme you choose, and the title will be shown as the title for the post. Change the date to your current time, and add categories as you want.
		```shell
		---
		layout: post
		title: "POST-TITLE"
		date: YYYY-MM-DD hh:mm:ss -0000
		categories: CATEGORY-1
		---
		```

	4. Add the formatted resume below the frontmatter.
	
* if you want to show your resume directly on the GitHub Pages: 
	1. Create or modify the index.md file in the root.
	
	2. Add the `layout: base`  YAML frontmatter on the top of the file, you can change the layout to the style you want.

	3. Add the formatted resume below the frontmatter.
	
* Now you can go on https://yourusername.github.io/ to check out your new website and online resume.


## More Resources
[Modern Technical Writing](https://www.amazon.ca/Modern-Technical-Writing-Introduction-Documentation-ebook/dp/B01A2QL9SS), by Andrew Etter.

[Markdown Tutorial](https://www.markdowntutorial.com/) for how to use Markdown.

[GitHub Documation](https://docs.github.com/en) to learn more GitHub functions.

  
  

## Authors and Acknowledgments
Thanks to Jesse Luoto for [README](https://github.com/jehna/readme-best-practices) template. And thanks [LICEcap](https://www.cockos.com/licecap/) for the gif generation and screen capture tool.

Thanks to [GitHub Docs](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site) for instructing me on how to create a Github Pages with Jekyll in the first place.

And thanks to Reviewers:
(insert group members for v2)


  

## FAQs

1. Why using Jekyll to host your resume?

* Using Jekyll with GitHub Pages offers several benefits, including:

	1.  Free Hosting: GitHub Pages provides free hosting for your Jekyll-powered website. This means you don't have to pay for a separate hosting service, and your website is automatically backed up and version-controlled by GitHub.
	
	3.  Easy Setup: GitHub Pages makes it easy to set up a Jekyll-powered website. You can create a new repository and select a Jekyll theme, or you can create a new Jekyll project from scratch and push it to GitHub.
	
	4.  Security: GitHub Pages provides HTTPS encryption for your website, which helps keep your website and your visitors' data secure.


2. Why the theme is not working?
* Make sure you use the correct layout syntax provided by the theme in your index.markdown.



