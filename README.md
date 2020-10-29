# The simplest app to plug anywhere

With this app you can use React, and any npm module you want, along with typescript.

This is all thanks to Parcel.

## Building

```sh
npm run build
```

You will see an bundle : `./build/release/<src.f69400.js>`

## Integrating

If you have an existing app, check how `build/release/index.html` is importing the bundle:

```html
<!DOCTYPE html><html lang="en"><head><meta charset="UTF-8"><meta name="viewport" content="width=device-width, initial-scale=1.0"><meta http-equiv="X-UA-Compatible" content="ie=edge"><title>TypeScript, React, Parcel Starter!</title></head><body> <div id="my-root"></div> <script src="src.ee870520.js" type="text/javascript"></script> </body></html>
```

The important part is this:

```html
<div id="my-root"></div> <script src="src.ee870520.js" type="text/javascript"></script>
```

You can either :

- copy paste the above snippet as is, and make sure to put the file `src.ee870520.js` in a publicly accessible dir
- rename the js file to something fixed like `my-app.js`, put it in a publicly accessible dir, and import it from your page.

**IMPORTANT**: make sure to match the `<div id="...">` attribute in your code snippet and in `index.tsx`. Otherwise react won't know where to mount.
