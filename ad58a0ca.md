---
title: Lexical scoping (JS)
date: 2021-11-02T09:34
tags: 
  - dev
  - javascript
  - compiler
---

Lexical scoping är en scoping-mekanism som innebär att tillgängligheten på
variabler bestäms av positionen av variabeln i nästlade scopes. Det betyder att
inom ett inre scope så kan du nå variabler från ett yttre scope, t.ex i exemplet
nedan kan variabeln ```outerVar``` nås i funktionen ```innerFunc```.

Exempel:
```js
function outerFunc() {
    let outerVar = 'Definierad i yttre scope';

    function innerFunc() {
        outerVar: // => 'Definierad i yttre scope'
    }
    
    innerFunc();
}

outerFunc();
```

Det kallas _lexical scoping_ (eller ibland _static scoping_) för att scopingen
görs i kompilatorn vid [[[8f00ffe5]]] (__lexical analysis_/_tokenization_),
alltså genom att parsa källkoden utan att exekvera den.
