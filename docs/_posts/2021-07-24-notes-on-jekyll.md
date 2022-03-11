---
layout: post
title:  "Notes on Jekyll"
date:   2021-07-24 22:24:55 +0900
categories: jekyll update
---

# (Prerequisites)

- install git https://git-scm.com/downloads
- install ruby https://www.ruby-lang.org/en/documentation/installation/
- install jekyll via bundler https://bundler.io/ 

jekyll install list https://jekyllrb.com/docs/installation/ 

-If errors appear during installation with bundler, try lowering the ruby version (currently using 2.7).

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
- Test locally with bundle exec jekyll serve 
- For local errors bundle add webrick 
- View locally at [http://localhost:4000](http://127.0.0.1:4000/blog/)

Article format `YEAR-MONTH-DAY-title.MARKUP`

Test html page at [/test](https://foxelas.github.io/blog/test)

- For posts / articles: 
	- Syntax for [Markdown](https://www.markdownguide.org/basic-syntax/)

- For styling: 
	- Dynamic content is provided with a language called [Liquid](https://shopify.github.io/liquid/)
	- Variable { { variable } } 
	- Logic statements, loops { % if statement % } 
	- To avoid printing whitespaces { % - else  - % }
	
--------------------------------------------

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}
--------------------------------------------

# Jekyll Links 

- [jekyll-docs](https://jekyllrb.com/docs/home)
- [jekyll-gh](https://github.com/jekyll/jekyll)
- [jekyll-talk](https://talk.jekyllrb.com/)

Update (2022/03/10): 
- Use [polyglot](https://github.com/untra/polyglot) for multiple languages 
- Minimize code with [jekyll-minifier](https://github.com/digitalsparky/jekyll-minifier)

- If a page does not build / builds partially, maybe the specific plugins are not included in Github pages. 
In such a case build the site locally and publish the _site folder.

