# sapper-template

The default [Sapper](https://github.com/sveltejs/sapper) template. To clone it and get started:

```bash
npx degit sveltejs/sapper-template my-app
cd my-app
npm install # or yarn!
npm run dev
```

Open up [localhost:3000](http://localhost:3000) and start clicking around.

## Reproduce bug one

> Anchor links don't jump to the correct position

Not seen in Chrome 67.0.3396.99

1. In Firefox 61.0.1...
1. Click on a link and it will appropriately jump you down to that portion of the page
1. Copy the url
1. Paste the url and hit <kbd>return</kbd>. The page will initially load and then jump back up to the top of the page.

![](screenshot.gif)

## Reproduce bug two

> Anchor links need the full path

This is appears in FF, Chrome and Safari

1. Navigate to <localhost:3000/blog>, click one of the links, which have an `href` of `#{post.slug}`
1. Instead of the normal behavior of appending `#<my-slug>` to the end of the url, it navigates to `localhost:3000/<my-slug>`.

See <https://github.com/mhkeller/anchor-test-two> for normal anchor browser behavior.
