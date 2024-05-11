

# Codebase for building this wiki

This wiki is built based on [git-wiki-theme repository](https://github.com/drassil/git-wiki-theme). To edit/fix git-wiki-theme core files, see [git-wiki documentation](https://github.com/Drassil/git-wiki) 

You can include the [official github wiki](https://help.github.com/articles/about-github-wikis/) as a submodule and enable the option in our conf file to use github wiki pages in git-wiki system, but it's an experimental feature and it implies less advantages and greater disadvantages for now.

You can open a public issue on [github](https://github.com/Drassil/git-wiki/issues) , 


# Customize git-wiki

From version 2.x Git-Wiki uses a **modular** architecture based on **components** and **"including hooks".**
This will allow you to **totally costumize** your wiki **adding new code** and/or **create your layout from scratch reusing every single piece** of git-wiki.

There are various methods to costumize and extends git-wiki, starting from the easiest one we will list them here:

## Change Wiki description info info in _config.yml.

```
title
description
logo_url
```

## Wiki themes

by default git-wiki includes some internal layout that you can set in your _config.yml to change your UI:

* [default theme](theme-default) (w3css)
* [lux theme](theme-lux) (bootstrap)
* [united theme](theme-united) (bootstrap)
* [github theme](theme-github) (bootstrap)



## Layout refactoring

Before working with layout refactoring you should learn:

* how to work with Jekyll: [https://jekyllrb.com/docs/](https://jekyllrb.com/docs/)
* which are the components of git-wiki, you can find them here: <https://github.com/Drassil/git-wiki-theme/tree/master/_includes>
* Take a look at git-wiki default layouts to understand how to build your: <https://github.com/Drassil/git-wiki-theme/tree/master/_layouts>

If you need to totally change the layout of your wiki you can create a custom file in _layout folder_ and reuse only components that you need in the place that you want.


You've just to change following config:

```
defaults:
 -
    scope:
      path: "" # an empty string here means all files in the project
    values:
      layout: "git-wiki-default"
 -
    scope:
      path: ""
      type: "pages"
    values:
      layout: "git-wiki-default"
```
  
replacing **layout: "git-wiki-default"** with name of your custom layout.


## Including hooks

If you need to extend git-wiki adding or replacing css rules, adding scripts or html elements you
can use the "including hooks" feature. It allows you to dynamically include a custom html code using the jekyll partials.
**NOTE**: Your file must be added inside the _include folder

### Style changes (head)

If you need a simple style change the easiest way to do it is including a custom css file that is able to add/overwrite default css rules.
  
To do it you can add in your _config.yml the following configuration:

```
inc_after_styles : "path/to/your/style.html" 
```
  
then in your _include folder you must add file defined above. It must be an html with the <link> elements inside.
  
For example: 

```HTML
<link rel="stylesheet" href="{{ 'assets/css/mystyle.css' | relative_url }}">
```
  
**NOTE**: as you can see we're using relative_url jekyll function allowing us to include the css file of our assets folder.



### Sidebar
  
If you need to add content inside sidebar of our default layout you can use following hook:

`inc_after_header: "my_sidebar_file.html"`

### Comments
  
If you need to add a comment component (for example disqus) you can use following hook:
  
`inc_after_content: "my_comments_file.html"`



# Prose.io
Prose.io provides useful editing tools and preview. However, it doesn't work with the current app access restrictions... something we can think about
```
Although you appear to have the correct authorization credentials, the `tsao-lab-UCB` organization has enabled OAuth App access restrictions, meaning that data access to third-parties is limited. For more information on these restrictions, including how to enable this app, visit https://docs.github.com/articles/restricting-access-to-your-organization-s-data/
```


# Work locally
* If you need to work on git-wiki locally before publish, then clone your wiki repo and follow this instructions from official github article: <https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/>. Git wiki already contains the Gemfile for local installations.
* You can also use our **docker files** to run git-wiki under **docker**, the easiest method is to run `docker-compose up` command in this folder (docker-compose build first before if you make any changes in dockerfile in .envfiles).
* If you are using mac, you might encounter nokogiri dependencies issue, which can be solved by adding right platform to both dockerfile and gemfile, I also had to add gem install kramdown-parser-gfm in gem file 



  
# Current known limitations

* You can't use the wiki internal link format: [[example]]. Please, use gh-pages links instead: \[example\](example) . It's a known jekyll limitation: <https://jekyllrb.com/docs/templates/>
* [How to setup the search feature](search-feature.md)?



# other wiki examples

If you have built a wiki with git-wiki, please edit this file and add your wiki link

* [aZerothCore](http://www.azerothcore.org/wiki/home)
* [River Architect](https://riverarchitect.github.io/RA_wiki/)
* [HW-Core JS Class](https://hw-core.github.io/js-lib-class/)
* [NestJS Yalc](https://www.drassil.org/nestjs-yalc/)
* [Agora Wiki](https://agoranomic.github.io/wiki/)
* [ClearlyDefined doc](https://docs.clearlydefined.io/)
* [ifbctag](https://ifbctag.github.io/labwiki)
* [sonbuildmeahouse](https://sonbuildmeahouse.github.io/)
* [lacroix](https://gihad.github.io/lacroix/)
* [NCSA Genomics](http://priyab2.github.io/git-wiki)
* [WoWGaming](https://wowgaming.github.io/wiki-en)
* [Talon Wiki](https://talon.wiki/)
* [Ornia](https://ornia.arcinas.info/)
* [Anoduck's Das Wiki](https://anoduck.github.io/wiki/)
* [JaxPlays](https://jaxplays.com)

