---
title: My first Blog Post
description: Learning how to use @nuxt/content to create a blog
img: scc.png
alt: my first blog post
author:
  name: Benjamin
  bio: All about Benjamin
  image: https://images.unsplash.com/.....
---
## This is a heading

This is some more info

### This is a sub heading

This is some more info

### This is another sub heading

This is some more info

## This is another heading

This is some more info

```js[my-first-blog-post.md]
export default {
  nuxt: 'is the best'
}
```
```html
<p>code styling is easy</p>
```

<info-box>
  <template #info-box>
    This is a vue component inside markdown using slots
  </template>
</info-box>
