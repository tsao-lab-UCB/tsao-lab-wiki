# Resources for building this wiki

This wiki is built based on [git-wiki-theme repository](https://github.com/drassil/git-wiki-theme). To edit/fix git-wiki-theme core files, see [git-wiki documentation](https://github.com/Drassil/git-wiki) 

You can include the [official github wiki](https://help.github.com/articles/about-github-wikis/) as a submodule and enable the option in our conf file to use github wiki pages in git-wiki system, but it's an experimental feature and it implies less advantages and greater disadvantages for now.

You can open a public issue on [github](https://github.com/Drassil/git-wiki/issues) , 

## Prose.io
Prose.io provides useful editing tools and preview. However, it doesn't work with the current app access restrictions...
```
Although you appear to have the correct authorization credentials, the `tsao-lab-UCB` organization has enabled OAuth App access restrictions, meaning that data access to third-parties is limited. For more information on these restrictions, including how to enable this app, visit https://docs.github.com/articles/restricting-access-to-your-organization-s-data/
```

## Work locally
* If you need to work on git-wiki locally before publish, then clone your wiki repo and follow this instructions  from official github article: <https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/>. Git wiki already contains the Gemfile for local installations.
* You can also use our **docker files** to run git-wiki under **docker**, the easiest method is to run `docker-compose up` command in this folder

## Configuration and customization

* [How to customize your wiki](customize.md)

* [How to setup the search feature](search-feature.md)

  
# Current known limitations

* You can't use the wiki internal link format: [[example]]. Please, use gh-pages links instead: \[example\](example) . It's a known jekyll limitation: <https://jekyllrb.com/docs/templates/>

