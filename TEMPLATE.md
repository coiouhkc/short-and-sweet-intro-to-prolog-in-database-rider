---
marp: true
title: Short and sweet intro to Prolog
description: Short and sweet intro to Prolog
theme: uncover
paginate: true
_paginate: false
header: "**Alexei Bratuhin** Short and Sweet intro to Prolog"
footer: ""



---

# Short and sweet intro to Prolog

## with application to Database-Rider

---

# Intro, reason & background

<!--

Would not it be cool to be able to test interconnections between database entities in simple manner? 

-->

---

# m-n Relationships

<style>
.container{
    display: flex;
}
.col{
    flex: 1;
}
</style>

<div class="container">

<div class="col">
Action <br/>
User @realpestano adds a tweet "dbunit rules!"
</div>

<div class="col">
Result

```
USER:
  - ID: $$x$$
    NAME: "@realpestano"
TWEET:
  - ID: abcdef12345
    CONTENT: "dbunit rules!"
    USER_ID: $$x$$
```
</div>

</div>


---

# Story time: Prolog

* PROgramming LOGic
* 1972
* Declarative*
* natural language processing, expert systems and many more

---

# Story time: Demo Prolog

https://swish.swi-prolog.org/
https://pika-lab.gitlab.io/tuprolog/2p-kt-web/

---

# Back to Database-Rider

### Theory

```
post(1, 'my first post', 'some description').
comment(1, 1, 'comment 1').
comment(2, 1, 'comment 2')
```

### Query

```
post(X, _, _), comment(_, X, 'comment 2')
```

---

# Database-Rider 

Use existing Java Prolog library to transform actual to theory and expected to query.

https://github.com/database-rider/database-rider/pull/531


---

# Q&A

---

# Links

* https://en.wikipedia.org/wiki/Prolog
* https://www.swi-prolog.org/
* http://swish.swi-prolog.org/
* https://en.wikipedia.org/wiki/Zebra_Puzzle
* https://github.com/DonaldKellett/Einsteins-Riddle-Prolog
* https://apice.unibo.it/xwiki/bin/view/Tuprolog/
* https://pika-lab.gitlab.io/tuprolog/2p-kt-web/
