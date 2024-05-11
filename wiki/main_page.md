---
redirect_from: /
published: true
---

# Welcome to Tsao-lab Wiki

This wiki is powered by git, and [github](https://pages.github.com/)/[gitlab](https://about.gitlab.com/product/pages/) pages!

A few key features:
* To add a new post, just click *add a new post* on the top right button. The format of each file is **Markdown and html** mixed together. 
* You can **edit** each page with the standard git editor (top row), prose.io (second row) or any kind of editor you prefer if you work locally. It might take few secs to minutes to your stuff to get published!
* Non-existent wiki page links are "[red](red.md)", you can **click on them to automatically create a new page**!
* Automatic generated **TOC** for each page
* Click **History** for showing the revision history of that document
* Leave **Comments** for your questions
* Search for documents using search engine on the top right!
* You can download the entire wiki for **offline** usage 


# Resources for building this wiki

This wiki is built based on [git-wiki-theme repository](https://github.com/drassil/git-wiki-theme). To edit/fix git-wiki-theme core files, see [git-wiki documentation](https://github.com/Drassil/git-wiki) 

You can include the [official github wiki](https://help.github.com/articles/about-github-wikis/) as a submodule and enable the option in our conf file to use github wiki pages in git-wiki system, but it's an experimental feature and it implies less advantages and greater disadvantages for now.

You can open a public issue on [github](https://github.com/Drassil/git-wiki/issues) , 

## Work locally
* If you need to work on git-wiki locally before publish, then clone your wiki repo and follow this instructions  from official github article: <https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/>. Git wiki already contains the Gemfile for local installations.
* You can also use our **docker files** to run git-wiki under **docker**, the easiest method is to run `docker-compose up` command in this folder

## Configuration and customization

* [How to customize your wiki](customize.md)

* [How to setup the search feature](search-feature.md)

  
# Current known limitations

* You can't use the wiki internal link format: [[example]]. Please, use gh-pages links instead: \[example\](example) . It's a known jekyll limitation: <https://jekyllrb.com/docs/templates/>



[MIT LICENSE](LICENSE)
