# Magento CMS pages as a tree structure

[![Build Status](https://secure.travis-ci.org/jreinke/magento-clever-cms.png?branch=master)](http://travis-ci.org/jreinke/magento-clever-cms)

![Clever CMS](http://i.imgur.com/3NOIN.jpg)

## Features
* CMS pages as a tree structure, drag & drop pages
* Restrict CMS pages access to customer groups (if enabled)
* Create 301 permanent redirects for old urls (if enabled)
* Manage a global tree and a store view independent tree
* Frontend navigation

## Installation

### Magento CE 1.6.x, 1.7.x

Install with [modgit](https://github.com/jreinke/modgit):

    $ cd /path/to/magento
    $ modgit init
    $ modgit -e README.md -e CHANGELOG.md clone clever-cms https://github.com/jreinke/magento-clever-cms.git

or download package manually:

* Download latest version [here](https://github.com/jreinke/magento-clever-cms/downloads)
* Unzip in Magento root folder
* Clean cache

### Magento CE 1.4.x, 1.5.x

**Compatibility of master branch is not guaranteed with versions of Magento above!**
**Please download/clone 1.2 branch**

Install with [modgit](https://github.com/jreinke/modgit):

    $ cd /path/to/magento
    $ modgit init
    $ modgit -e README.md -e CHANGELOG.md clone clever-cms https://github.com/jreinke/magento-clever-cms.git --branch 1.2

or download package manually:

* Download 1.2.x version [here](https://github.com/jreinke/magento-clever-cms/tags)
* Unzip in Magento root folder
* Clean cache

## Full overview

I wrote an article on my blog for full extension overview, [click here](http://www.johannreinke.com/en/2012/01/10/magento-cms-pages-in-a-tree-structure/).


## Manadev
For comability with the manadev layered navigation a foreign key must be updated

On the table m_seo_url delete the foreign key FK_m_seo_url_cms_page_id
And add a new key with the name: FK_m_seo_url_cms_page_tree_id
own field: cms_page_id
other table: cms_page_tree
other field: page_id
