---
title: Tailwind CSS
author: shimseonjo
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
npx tailwindcss init --full
```
tailwind.config.js  파일 생성됨 
설정된 모든 클래스를 확인할 수 있다.

tailwind.config.js 파일에 내용을 추가했다면... 다시 output.css를 작성한다. 

```js
<!-- tailwind.config.js  -->
fontSize: {
mammoth: '8rem',
xs: '0.75rem',
},
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

내용이 추가된 output.css를 이용하여 적용된 스타일을 확인
```html
<!doctype html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="/output.css" rel="stylesheet">
</head>
<body>
  <h1 class="text-mammoth font-bold underline">
    Hello world!
  </h1>
</body>
</html>
```

### 기본설정을 놔두고 추가내용만 작성하여 사용
tailwind.config.js 파일을 tailwind-default.config.js 로 이름 변경

```bash
npx tailwindcss init
```
새로운 tailwind.config.js 파일을 생성

```js
module.exports = {
  theme: {
    extend: {
      colors: {
        primary: '#FF6363',
        secondary: {
          100: '#E2E2D5',
          200: '#888883',
        }
      }
    },
  },

}
```

```bash
npx tailwindcss -i ./src/input.css -o ./src/output.css --watch
```
다시 output.css에 적용해서 사용한다.