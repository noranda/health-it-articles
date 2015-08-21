# Health IT Articles

An [open source list] of health IT articles.

### Use git to make changes

Fork a copy of the repo from GitHub, make the changes you want (see below), then stage, commit, and push your changes as follows:

```
git add <file you've changed>
git commit -m "these are the changes I've made"
git push origin master
```

If you'd like to view your changes before making a pull request, you can do so by starting a [Jekyll] server:

```
jekyll serve
```

Finally, submit a [pull request] to merge your changes into the repo.

### Adding an Article

Create a new `md` file in the `_posts\` folder using the following naming convention:

```
YYYY-MM-DD-article-name.md
```

The date should correspond to the date the article was published. Next, use the following template to add the article information your new file:

```
---
layout: article
title: ARTICLE TITLE
article_url: ARTICLE URL
author: ARTICLE AUTHOR
publisher: ARTICLE PUBLISHER
publisher_url: ARTICLE PUBLISHER URL
published_date: YYYY-MM-DD
tags:
  - your
  - tags
---

INFORMATION ABOUT THE ARTICLE
```

It is important to include the `---` dashes. Also do not use a `:` except in a URL. Save the file and run the tags rakefile (see below).

### Editing an article

To edit an article, find the article file you'd like to edit in the `_posts/` folder and make the changes.

### Tags

If you changed any of the tags either by adding or deleting an article, run the following to update the tag files:

```sh
$ rake tags:generate
```

----
### License

MIT

[pull request]:https://github.com/noranda/health-it-articles/pulls
[open source list]:http://noranda.github.io/health-it-articles/
[Jekyll]:http://jekyllrb.com/
