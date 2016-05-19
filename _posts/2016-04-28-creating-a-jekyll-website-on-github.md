---
title: "Creating a Jekyll Website on GitHub"
header:
    overlay_color: "#777"
excerpt: "In this post, I delve into the journey I took when creating a personal website using jekyll and github. I discuss why I wanted to make a personal website, what my intentions are in having one, and how I went about creating it. Topics include github, markdown, jekyll, and ruby gems."
categories:
    - Guides
    - Web
tags:
    - Jekyll
    - GitHub
    - GitHub Pages
    - Markdown
    - Learning
    - Ruby
    - RubyGems
    - Personal Experience
---
Ever since I got back from the Spring Open House at Appalachian State, I knew that I wanted to create a website that hosted my portfolio. I wanted to show my professors and friends, and future employers the things I've been working on, but I didn't know how to create a website to do that. I had heard about GitHub pages a while ago when I first created my account on GitHub, but I hadn't done much research on it until a few days ago.

### What are GitHub Pages?
GitHub offers free web hosting on its servers, but the caveat is that the website repositories must be hosted publicly. All files are freely accessible to everyone, which obviously isn't the best scenario for all people. You have the option of using your own domain name, but you have to have already purchased it from a domain name provider, otherwise, you'll be restricted to a subdomain along the following format: `sitename.github.io`.

For me, free hosting under GitHub was perfect. So, I spent some time following the GitHub Pages help files, and after seeing how limited the automatic page generator was, I knew I needed another option. I'm not comfortable enough with web design to make an impressive website on my own, so I turned to Jekyll. 

### What is Jekyll?
Jekyll is a Ruby gem that aids in the creation of blogs and static pages, and is what powers GitHub Pages. It's not easy to setup on a Windows platform, but for other platforms like Mac OS or Linux, it's pretty straight forward. I ended up following [this](http://jekyll-windows.juthilo.com/) guide on how to get it set up on my system, and I didn't run into any issues. If you're on anything other than Windows, you can follow [this](https://jekyllrb.com/docs/installation/) guide. I'll explain in more detail later on how to get started with Jekyll.

### What's a Ruby Gem?
Essentially, you need to have Ruby installed. Jekyll uses it to do a lot of the heavy lifting when generating sites. There are a multitude of Ruby 'gems' jekyll uses, which are kind of like individual programs that can be run from the command line. These gems are installed by typing  `gem install` followed by the name of the gem into the command prompt, and was the most exciting and bizarre thing to me. It was like magic! How does the application that installs gems know where to find the gems, and where does it save them? How does a simple command *just work*?

It turns out that a lot of Gems are hosted on a website called _RubyGems.org_, but individuals can also host gems on their own servers. When you type in `gem install` into the command prompt, a connection is made between your computer and the server where the gem is located, and the file is downloaded onto your machine. The `gem install` command is provided by the Ruby Development Kit, which is downloaded as part of the Jekyll Windows installation guide. The gem itself is saved to a file location defined as the INSTALLATION DIRECTORY when you use the command `gem environment`.

### How do I Keep Ruby Gems Updated?
Jekyll uses a lot of Ruby gems when generating a website, and if there are any conflicts with any of them, it can cause the build to fail. Using the command `gem update && gem clean` for each of Jekyll's dependencies will bring them up-to-date, but it can be time consuming and tedious. 

A convenient solution is to install the ruby gem, 'Bundler,' which manages collections of gems as specified in the `GemFile` included in your project. Once Bundler first uses the `GemFile` included in the theme you chose for the website, it will generate a `GemFile.lock`, which is the build output of all the gems Bundler installed and updated. The latest version of each gem is listed there, and so for consecutive uses of `bundle update`, bundle will use the `GemFile.lock` file instead.

If you use Bundler, then it is recommended to call Jekyll commands through Bundler. Calling `bundle exec jekyll` followed by the Jekyll command will eliminate any gem version issues, and will help prevent any build problems Jekyll has as a result of out-of-date gems.

### So How do I Get Started Making a Website?
Once Ruby and the Ruby Development Kit are installed, you'll need to create a repository on GitHub that stores your website's files. The repository has to be public, and the name must  follow the format `sitename.github.io`. The `sitename` portion of the url can be whatever you want it to be, as long as it isn't taken by anyone else. The name of the repository will become the url for your website, unless you wish to use a custom domain name. More information on using custom domains for GitHub pages can be found [here](https://help.github.com/articles/using-a-custom-domain-with-github-pages/).

With a repository set up, you can now start creating your Jekyll website. If you are interested in creating a website from scratch, you'll want to learn about the explicit [directory structure](https://jekyllrb.com/docs/structure/) Jekyll uses, [liquid templates](https://jekyllrb.com/docs/templates/), and YAML. Knowing HTML, CSS, and Javascript will be useful in creating a personalized theme for yourself. If you're not going to use a  predefined theme though, you'll have a lot of work ahead of you.

<div class="notice--info">
<p>
<strong>Aside</strong>: Pages, posts, and collections you see on a Jekyll website use layouts, included page snippets, and data files as convenience tools for maintaining a specific theme throughout your website. Layouts and includes are HTML pages that have been styled with CSS and use liquid to manage the content they encapsulate. 
</p>
<p>
YAML is used to configure the website's settings, and is used both in the _config.yml file as well as YAML Front Matter. The _config.yml file holds default settings that won't normally be changed frequently, and Front Matter is YAML that's included in the header of collections, pages, and posts where custom information is needed.
</p>
</div>

If you're not interested in creating a website from scratch, you'll need someone else to create a theme for you. You can choose from a list of themes [here](https://github.com/jekyll/jekyll/wiki/themes), but take note of the licence the theme has. Licences restrict how software can be used, and are important to understand. The theme I use for this website is [Minimal  Mistakes](https://mmistakes.github.io/minimal-mistakes/), which has great documentation explaining how to use each of the features the theme provides. The theme you choose will most likely have similar documentation for what it offers and how to use it.

Installing the theme hosted on GitHub into a new repository is pretty simple. In general, you would need to fork the theme's repository, then change the name of the fork to `sitename.github.io` where the `sitename` is replaced with something unique that you like. Your website won't be live unless you force an update, which is done by committing a change to the repository.

### So How do I use Jekyll?
Once your have the theme installed into your repository, you have two options for using Jekyll. Jekyll can be used directly through the GitHub web interface, or you can clone the repository to your machine and develop your website locally. Both methods are similar in the workflow they require, but an important distinction should be made. Working directly through the GitHub web interface will causes all the changes you make to the website go live immediately, whereas using Jekyll locally will not. The changes you make locally have to be pushed into the remote repository before they go live.

For both methods of development, you'll need to understand the way Jekyll works. In most cases, Jekyll will generate an HTML file for every markdown file you've created and placed in the proper directory. For the pages that aren't automatically generated, you'll have to specify for Jekyll to generate the page for it in `_config.yml`. This is usually done by setting the `output` value to `true` for the site type (page, post, or collection). To learn about the directory structure Jekyll uses, look [here](https://jekyllrb.com/docs/structure/).

Creating markdown files is the bread and butter of generating a Jekyll site, and is what makes Jekyll so appealing to non-web designers. A markdown file is a specially formatted file that website content is written into, and is similar to writing forum responses in BB Code. For an overview of how to use markdown, I encourage you to look [here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet). Another useful resource is [this](http://kramdown.gettalong.org/quickref.html) page, as some themes are using Kramdown.
{: .notice--info}

There are three types of web pages Jekyll works with: Collections, Pages, and Posts. Pages are individual web pages that do not share a relationship with other pages, and are usually things like an 'about' or 'contact' page. Posts are used for blog entries, and collections contain a series of pages that share a relationship with one another, like a cookbook full of recipes.

* To create a page, make a markdown file containing the proper Front Matter, and save it in the `_pages` folder found in the base directory.
* To create a post, make a markdown file containing the proper Front Matter, and save it in the `_posts` folder found in the base directory with a name in the following convention: `YYYY-MM-DD-post-title.md`. The naming convention can be different than what I described, so refer to the theme you chose for instructions.
* To create a collection, you'll need to first add the collection information to `_config.yml`, and then create a folder in the base directory with the collection name. Create markdown files for each page you want in the collection, and save them in the folder containing the collection name. The navigation between pages in a collection is based on the alphanumeric order of files in the collection folder, so name the files accordingly. A good solution is to add a number in front of the actual name of the file, like `01-file-name.md`.

Each theme might require specific Front Matter for the markdown files you create, so refer to the theme you chose for instructions on how to create pages, posts, and collections.

In order to have Jekyll process your markdown files, the method to do so depends on whether you're working remotely or locally. If you're developing your website locally, you'll need to run the command `bundle exec jekyll serve` in the command prompt while at your website's directory. If you aren't using bundle, run `jekyll serve` instead. This will cause Jekyll to launch your website to `localhost:4000`, which is where you can preview it before it goes live. To have the changes you make go live, you'll need to push the commits to master in the remote repository on github. If you're working remotely, Jekyll will automatically process your files as they're committed, as long as they're in the correct folders.

**Tip**: Use two configuration files when creating your website; one for development and one for the live website. There are many benefits to having two, such as having a different base urls and analytics settings for each. To use an alternate configuration file, use this command to serve your website `bundle exec jekyll serve --config` followed by the name and extension of the development configuration file.
{: .notice--info}

### In Closing
With the knowledge of how to install Ruby and its development kit on your system, and how to acquire Jekyll and the necessary Ruby gems it uses, you've learned how to prepare your system to start creating websites hosted on GitHub. Furthermore, you've learned about how to use Jekyll, acquire a theme, and how to create markdown content that Jekyll outputs as HTML files. All that's left is to add your personal touch to the website you want to make, and populate it with content you want others to see. There will still be things to learn and master, but that's apart of the journey for anything that's worthwhile pursuing.
