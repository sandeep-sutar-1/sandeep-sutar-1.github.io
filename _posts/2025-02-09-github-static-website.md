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
During installation, install all three options provided - 
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
Create a new Jekyll site.
```BASH
C:\Users\Sandeep\sandeep-sutar-1.github.io> jekyll new my-jekyll-site
Running bundle install in C:/Users/Sandeep/sandeep-sutar-1.github.io/my-jekyll-site... 
  Bundler: Fetching gem metadata from https://rubygems.org/...........
  Bundler: Resolving dependencies...
  Bundler: Bundle complete! 7 Gemfile dependencies, 41 gems now installed.
  Bundler: Use `bundle info [gemname]` to see where a bundled gem is installed.
New jekyll site installed in C:/Users/Sandeep/sandeep-sutar-1.github.io/my-jekyll-site. 
```
Update the `_config.yml` file as per your wish.

# Host the website on GitHub pages.
Push your code to GitHub repository.

# References
- If you want to learn more about Jekyll, visit [Giraffe Academy](https://www.youtube.com/playlist?list=PLLAZ4kZ9dFpOPV5C5Ay0pHaa0RJFhcmcB) on Youtube.
- Visit [Jekyll Minima](https://github.com/jekyll/minima/blob/master/README.md) on GitHub to know more about customization options for this theme.