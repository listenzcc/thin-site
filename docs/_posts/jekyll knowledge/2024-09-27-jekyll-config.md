---
layout: single
title: Jekyll configuration
date: 2024-9-27
categories: jekyll web gem
toc: true
---
How the jekyll is installed and is configured.

## Jekyll install and startup

```powershell
# Install Jekyll and startup example

gem install bundler jekyll
jekyll new my-awesome-site
cd my-awesome-site
bundle exec jekyll serve
```

url: <https://jekyllrb.com/>

## Gem configuration

### Table of contents

```yaml
# Configuration
# Add jekyll-toc plugin in your site's Gemfile, and run bundle install.
# Gemfile
gem 'jekyll-toc'

# Add jekyll-toc to the gems: section in your site's _config.yml.
# _config.yml
plugins:
- jekyll-toc

# Set toc: true in posts for which you want the TOC to appear.
# [post].md
---
layout: post
title: "Welcome to Jekyll!"
toc: true
---
```

url: <https://github.com/toshimaru/jekyll-toc>

## Syntax highlight

The Jekyll uses rouge for syntax highlight the code blocks in the .md documents.
The rouge is the dependent of the Jekyll, the script checks the rouge installation and help

```powershell
# List the rouge supporting files
rougify list

# Rouge style help
rougify help style

# Export the syntax.css of monokai.sublime
rougify style monokai.sublime > syntax.css
```


Here is some example:

```python
# Python script example
import time

def print_now():
    ct = time.ctime()
    print(f'Now is {ct}')

print_now()
```

```javascript
// Javascript script example
let array;
array = new Array(3).fill(0).map(_ => new Datetime())
console.log(array)
```
