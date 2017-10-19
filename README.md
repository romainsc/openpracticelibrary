# Open Practice Library

## About

Red Hat Open Innovation Labs team is creating an open practice library! To learn more, see [about.md](content/page/about.md).

## Adding Content

### Techniques

Create a new markdown file in `/content/techniques`. If you have hugo installed, you can run `hugo new techniques/my_new_technique.md`.

### Pages

Create a new markdown file in `/content/page`. If you have hugo installed, you can run `hugo new page/my_new_page.md`.

To display the page in the site menu, include `menu: main` in the front matter at the top of the file.

Open Practice Library is built with [Hugo](http://gohugo.io/) and the [Minimo theme](https://minimo.netlify.com/). To run it locally:

- Check out this repo.
- [Install Hugo](https://gohugo.io/getting-started/installing/).
- Run `hugo server` to to run the site locally.

Alternately, you can run `hugo server -D` to include drafts.
