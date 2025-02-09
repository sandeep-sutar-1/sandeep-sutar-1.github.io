---
layout: post
title:  "How I published this static website on GitHub using Jekyll."
date:   2025-02-09 12:59:11 -0700
categories: Information Technology
---

__Table of Contents__
* 
{:toc}

---
<BR>

# Download and Install Ruby
Download Ruby gems installer 3.3.7-1-x64 from [rubyinstaller.org](https://rubyinstaller.org/downloads/) and install Ruby. 
During the installation, install all three options provided - 
1. MSYSY2 base installation
2. MSYSY2 system update
3. MSYSY2 and MINGW development toolchain

Open Command Prompt and verify the install by running below command.
```BASH
C:\Users\Sandeep>ruby -v
ruby 3.3.7 (2025-01-15 revision be31f993d7) [x64-mingw-ucrt]
```

# Download and Install Jekyll.
Open Command Prompt and install Jekyll.
```BASH
C:\Users\Sandeep>gem install jekyll bundler
```

Verify the install by running below command.
```BASH
C:\Users\Sandeep>jekyll -v
jekyll 4.4.1
```

# Setup static website.
Open Command Prompt and create a new Jekyll site.
```BASH
cd "C:\Users\Sandeep\Desktop\"
C:\Users\Sandeep\Desktop> jekyll new my-website
Running bundle install in C:\Users\Sandeep\Desktop\my-website... 
  Bundler: Fetching gem metadata from https://rubygems.org/...........
  Bundler: Resolving dependencies...
  Bundler: Bundle complete! 7 Gemfile dependencies, 41 gems now installed.
  Bundler: Use `bundle info [gemname]` to see where a bundled gem is installed.
New jekyll site installed in C:\Users\Sandeep\Desktop\my-website. 
```
Update the `_config.yml` file with with information.

Customize your website theme and add blog posts if you wish.

Launch jekyll website on `localhost:4000` by running below command and visit this url on your browser to test.
```BASH
bundle exec jekyll serve
```

# Setup new GitHub repository.
Create new GitHub repository with special name `gh-user-name.github.io`. e.g. `sandeep-sutar-1.github.io`.
Set visibility to public.
Go to repository Settings --> Pages --> Build and deployment. Select source `Deploy from a Branch`. Set branch to `main`.

Open git bash on your local machine and clone the new repository.
```BASH
$ cd Desktop/GitHub\ Repositories/
$ git clone https://github.com/sandeep-sutar-1/sandeep-sutar-1.github.io.git
```

Create and checkout a new branch `gh-pages`, copy all the files from `C:\Users\Sandeep\Desktop\my-website` and push the changes to remote.
```BASH
$ cd sandeep-sutar-1.github.io/
$ git checkout -b gh-pages
Switched to a new branch 'gh-pages'
$ mv C:/Users/Sandeep/Desktop/my-website/. .
$ git add *
$ git commit -m "Initial commit"
$ git push origin gh-pages
```

Go to repository Settings --> Pages --> Build and deployment. Select source `Deploy from a Branch`. Set branch to `gh-pages`.

Visit your website on github pages by opening URL on `https://sandeep-sutar-1.github.io` in browser.

# References
- If you want to learn more about Jekyll, visit [Giraffe Academy](https://www.youtube.com/playlist?list=PLLAZ4kZ9dFpOPV5C5Ay0pHaa0RJFhcmcB) on Youtube.
- Visit [Jekyll Minima](https://github.com/jekyll/minima/blob/master/README.md) on GitHub to know more about customization options for this theme.