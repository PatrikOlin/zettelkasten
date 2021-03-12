---
title: console.log destructuring
date: 2021-03-12T14:28
slug: consolelog-destructuring
tags: 
  - dev
  - js/ts
---

I javascript/typescript kan man använda destructuring i console.log() för att
enkelt hålla koll på vilken variabel det är som man loggar.

Exempel:

Vi har en variabel, `debounce`, som vi vill logga. På klassiskt vis skulle man
göra något i den här stilen:

`
const debounce = 300
console.log('debounce', debounce)
`

och då få ut `debounce 300` i console. Med destructuring kan man göra såhär
istället:

`
const debounce = 300
console.log({ debounce })
`

och få ut `{debounce: 300}` i console, dvs man får med både värdet och variabelnamnet.


