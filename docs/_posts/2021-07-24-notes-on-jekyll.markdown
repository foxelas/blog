---
layout: post
title:  "Notes on Jekyll"
date:   2021-07-24 22:24:55 +0900
categories: jekyll update
---

# (Prequisites)

- install git https://git-scm.com/downloads
- install ruby https://www.ruby-lang.org/en/documentation/installation/
- install jekyll via bundler https://bundler.io/ 

jekyll install list https://jekyllrb.com/docs/installation/ 

# Preparation 
- Create a new repository 
- Open Git Bash and cd to the repo 
- Make a docs dir  mkdir docs OR 
	- Make a gh-pages branch git checkout --orphan gh-pages 
- Run jekyll new . (Needs to be an empty dir) 
- Open the Gemfile
- Modify to comment line gem "jekyll", "~>version"
- Modify to uncomment line with gem "github-pages", group: :jekyll_plugin 
- Modify to add gh-pages version from dependencies at https://pages.github.com/versions/   
	- gem "github-pages", "~> 215", group: :jekyll_plugins
- Save and close Gemfile 
- Run bundle update 
- Update _config.yml
- Add files, commit and push 
- Check deployment from Github browser menu
- Update the site with jekyll serve 

Article format `YEAR-MONTH-DAY-title.MARKUP`

--------------------------------------------

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
