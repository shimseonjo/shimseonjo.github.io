---
title: Emmet
author: shimseonjo
date: 2024-01-06
category: Doc
layout: post
permalink: /Emmet
---
[Emmet](https://emmet.io/)  
[mdn](https://developer.mozilla.org/ko/)

#### html 기본 생성
```html
#(항목 선택은 tab)
! or html 
```
#### 하위 요소 생성 : >
```css
nav > u l > li
```

#### 동급 요소 생성 : +
```css
div + p + bq
```

#### 반복 : *
```css
ul > li * 5
```

#### class : .
```css
li.item * 3
```

#### id : \#
```css
ul#menu > li.item * 3
```

#### 그룹 : ()
```css
.container > (header > nav > ul > li * 5 > a) + ( #content > section ) + footer
```

#### 속성 : []
```css
td[title="name" colspan="5"]
```

#### 텍스트 : {텍스트}
```css
a.button{Click Me}
```

#### 넘버링 : $
```css
ul.list > li.item $ * 5 > {$}
```
