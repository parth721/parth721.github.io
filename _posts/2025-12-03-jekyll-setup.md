---
layout: post
title: Jekyll Setup
date: 2025-12-02 10:00:00 +0530
categories: experience
---
Device : Ubuntu25.04

Always use RVM(Ruby version manager) or package manager `rbenv` to avoid permission issues.  

1. **Install ruby** 
```sh
sudo apt update
sudo apt install ruby-full build-essential zlib1g-dev
```
check version (Ruby3.0+ onwards removed webrick which was needed by jekyll so maually need to be installed)
```sh
ruby -v
```


2. **setup Gem installation directory :** <br>
Ruby will install libraries in your user folder, not the system folder.
```sh
echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

3. **Write Gemfile inside the Project root folder**
```sh
source "https://rubygems.org"
gem "github-pages", group: :jekyll_plugins
gem "webrick"
```

4. **Install Dependencies**
```sh
bundle install
```

5. **Create `.gitignore` and add the folders just created after previous step**
```sh
_site/
vendor/
.bundle/
.sass-cache/
.jekyll-cache/
#ignore Gemfile & Gemfile.lock
```

6. **Start the Server**
```sh
bundle exec jekyll serve
```

---

## Q&A

1. **Differnce between Gem, Ruby, Bundle ?**
2. **Why package manager are needed to avoid permission issue ?**
3. **Why echo commands are used here for Gem installation directory ?**
4. **Why webrick removed from ruby3.0+ but not from jekyll ?**

---

