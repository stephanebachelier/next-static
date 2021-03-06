[![styled with prettier](https://img.shields.io/badge/styled_with-prettier-ff69b4.svg)](https://github.com/prettier/prettier)

# Next Static Blog
__✨ Start static then go server rendered when you need to ✨__

A simple static blog powered by [next.js](https://github.com/zeit/next.js).

## Why
* I found other SSG (Static Site Generator) to be too much for what I need
* I wanted to be able to transition to a dynamic site easily if need be and next.js is a great existing SSR (Server Side Render) framework.

## Usage
* `yarn`
* `yarn run export`
* `cd out`
* `now`

### Adding a Post
* Create a `.js` file in `posts`.
* Export an object that contains post content/metadata
```js
module.exports =  {
  title: 'Title',
  slug: 'slug',
  author: 'Your Name',
  date: new Date().toString(),
  tags: [
    'tags',
    'go here'
  ],
  body: `
  ## Post
  Use markdown to _write_ your post
  Here's some code:
  \`\`\`javascript
  const a = 'thing';
  \`\`\`
  `
};
```
* Inside `./posts/index.js` require your new post and add it to the exported array.
* Re-run `yarn run export` to build your new site.
