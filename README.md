# search

This plugin is a default plugin for GitBook, it adds an interactive search bar to your book.

This plugin is backend agnostic.

### Disable this plugin

This is a default plugin and it can be disabled using a `book.json` configuration:

```
{
    plugins: ["-search"]
}
```

### Backends

| Backend | Plugin Name | Description |
| ------- | ----------- | ----------- |
| [Lunr](https://github.com/GitbookIO/plugin-lunr) | `lunr` | Index the content into a local/offlien index |
| [Algolia](https://github.com/GitbookIO/plugin-algolia) | `algolia` | Index the content in Algolia |

### Search options

Most backends for the `plugin-search` will support a range of common configuration listed below. **You should check the description of each backend in case some do not support some options**.


#### Adding keywords to a page

You can specify explicit keywords for any page. When searching for these keywords, the page will should rank higher in the results.

```md
---
search:
    keywords: ['keyword1', 'keyword2', 'etc.']
---

# My Page

This page should be among the first search results for "keyword1".
```

#### Disabling indexing of a page

You can disable the indexing of a specific page by adding a YAML header to the page:

```md
---
search: false
---

<<<<<<< HEAD
# My Page

This page should not appear in the search results.
```
=======
{% hint style="warning" %}
Rigging Artists/ Aspiring Rigging Artists have been struggling for so long because there is literally no place to learn rigging properly, even Autodesk has not given much content other than some videos which are far more advanced for junior/fresher rigging artists.

We mean to create a platform which can help and make it easy for everyone to learn rigging easily with short articles and videos! We are collecting information and study materials everyday to help you find everything at one place!
{% endhint %}

>>>>>>> parent of ac8dcfe (GitBook: [#6] No subject)
