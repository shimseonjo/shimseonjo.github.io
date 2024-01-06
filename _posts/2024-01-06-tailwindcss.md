---
title: Tailwind CSS
author: shimseonjo
date: 2024-01-06
category: Doc
layout: post
permalink: /TailwindCSS
---
[Tailwind CSS](https://tailwindcss.com/)
## CDN 사용
```html
<!doctype html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
</body>
</html>
```

## Tailwind CLI
```bash
npm install -D tailwindcss
npx tailwindcss init
```
```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```
```css
<!-- src/input.css -->
@tailwind base;
@tailwind components;
@tailwind utilities;
```
```bash
npx tailwindcss -i ./src/input.css -o ./src/output.css --watch
```
```html
<!doctype html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="/output.css" rel="stylesheet">
</head>
<body>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
</body>
</html>
```