# NewsNerdery.organization
## Local Development
### Before you start
We build the site using [Hugo](https://gohugo.io/). If you have `brew` installed, simply run `brew install hugo`.

Hugo also has tutorials for [Mac](https://gohugo.io/tutorials/installing-on-mac/) and [Windows](https://gohugo.io/tutorials/installing-on-windows/).

### Running the server locally
Navigate in a terminal window to the folder containing the cloned or forked instance of NewsNerdery.org and run `hugo server`. Hugo should give you a URL like `http://localhost:1313/` where you will now find the site.

Updates made to Hugo files will be reflected instantly in your browser. Try it by modifying a file within `content/onepage/`.

### Adding a section to the website
NewsNerdery.org currently exists on a single page. Sections on this page are configured through `content/onepage` and ordered based on their filename. 

### Composing text for NewsNerdery.org
Text can be written in raw HTML or markdown. Hugo uses the [BlackFriday renderer(https://github.com/russross/blackfriday) with an extension to support Github-style checklists, like this one:

- [x] Find a static site generator for News Nerdery.org

Hugo also supports code highlighting. To highlight a block of HTML within your Hugo file, you would include a chunk of markdown like this:

```css
body {
  font-family: "Noto Sans", sans-serif;
}
```

```html
<p>
  <strong>HTML!!!</strong>
</p>
```

### Optional author parameter
By default very little metadata is shown for blocks on NewsNerdery.org. But if you add an `author: Joe Journo` to the parameters, we'll tag the post as being by that value.

For instance, this post file:

```
---
date: 2016-11-16
author: "Joe Journo"
---
## A cool post
```
Would be rendered as:
![screen shot 2016-11-16 at 3 42 59 pm](https://cloud.githubusercontent.com/assets/1636964/20365018/6364195e-ac13-11e6-98fc-a65b2218c42e.png)

## Deploying changes
To deploy changes, you'll need to do two things. 

1. Build the site for distribution with `hugo -d dist`.
1. Run the deploy script with `./deploy.sh`.

