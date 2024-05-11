---
redirect_from: /
published: true
---

# Welcome to Tsao-lab Wiki

This wiki is powered by Git, and [GitHub](https://pages.github.com/)/[GitLab](https://about.gitlab.com/product/pages/) Pages!

A few key features:
- To add a new post, simply click on **add a new post** at the top right button. The format of each file is a mixture of **Markdown and HTML**. It might take a few minutes for your content to get published!
- You can **edit** each page using the standard Git editor (top row), Prose.io (second row), or any preferred editor if you're working locally.
- Non-existent wiki page links are displayed in "[red](red.md)" (in Light mode); you can click on them to **automatically create a new page**!
- Automatic generation of a **Table of Contents (TOC)** for each page.
- Click on **History** to view the revision history of a document.
- Leave **Comments** for any questions you may have.
- You can search using **search engine** at the top right!
- You can download the entire wiki for **offline** usage and work locally 


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
