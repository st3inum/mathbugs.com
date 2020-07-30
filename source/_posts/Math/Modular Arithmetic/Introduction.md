---
title: Introduction
date: 2020-07-30 02:09:04
tags: discrete-math , math
---

মডুলার অ্যারিথমেটিক নিয়ে পড়ার আগে আমরা কিছু জিনিস রিক্যাপ করে নেই , যেগুলা আমরা ক্লাস ফাইভে পড়ে এসেছি । 

`ভাজ্য = ভাজক × ভাগফল + ভাগশেষ` বা, `Dividend = Divisor × Quotient + Remainder`

অনেকের যদি কোনটা কি জিনিস মনে না থাকে তাহলে পুরানো বইয়ের পাতা উলটে দেখতে পার , আর [গুগল](google.com) মামা তো আছেই । 

এবার অনেকর মনে প্রশ্ন আসবে , অমুক প্রবলেম তো সহজেই পাটিগণিত / সাধারণ নিয়মে সল্ভ করে  ফেলা যায় , তাহলে এসব ম্যাথ করার জন্য মডুলার অ্যারিথমেটিক কেন শিখবো? তার উপর এটা তো একটা কঠিন টপিক । 

তাদের জন্য বলে রাখা, মডুলার অ্যারিথমেটিক হল এসব সাধারণ নিয়মগুলোর একটা কম্প্যাক্ট ফর্ম । তাই এভাবে করলে সহজেই অনেক প্রবলেম সল্ভ করে ফেলা যায় । যেগুলো কিনা সাধারণ ভাবে করলে অনেক বড় হয়ে যেত ।  আর সত্যি কথা বলতে মানুষকে কোন ম্যাথের সলিউশন বুঝাতে গেলে বেশি লেখা দেখলে ভয় পেয়ে যায়। কিন্তু মডুলার অ্যারিথমেটিক দিয়ে সল্ভ করলে কয়েক লাইনে হয়ে যায় বলে তারা ভয় পায় না। (just kidding :v ) 



## Definition:

আমরা অনেক সময় দেখে থাকি $a \text{ (mod b)}$ । এর মানে কি? সহজ করে বলতে গেলে এর মানে হল `a` কে `b` দিয়ে ভাগ করলে যেই ভাগশেষ থাকবে সেই সংখ্যাটা ।  উদাহরণস্বরূপ $5 \text{ (mod 3)}=2$

এখানে `mod` সাইনটা আসলে `modulo(মডুলো)` শব্দের সংক্ষিপ্ত রূপ । 

আমরা আবার অনেকসময় দেখে থাকি $a\equiv b \text{ (mod m)}$ এর মানেই বা কি? 

কখনো যদি $a \text{ (mod m)}=b \text{ (mod m)}$ হয় , তখন আমরা সংক্ষেপে লিখতে পারি $a\equiv b \text{ (mod m)}$ । এবং এটাকে পড়তে হয় `"a is congruent to b modulo m"` এভাবে ।  

এটাকে আমরা আরও একভাবে সংজ্ঞায়িত করতে পারি , যদি $(a-b)$ , $m$ দিয়ে নিঃশেষে ভাগ যায়, তাহলে আমরা লিখতে পারি $a\equiv b \text{ (mod m)}$ ।

আসলে দুইটা সংজ্ঞাই একই , একটু চিন্তা করলে বুঝতে পারবা। 



## Properties:

আমরা কোন সমীকরণের দুইপাশে যেমন একই সংখ্যা দিয়ে যোগ , বিয়োগ, গুন  করতে পারি ঠিক তেমনি আমরা মডুলার অ্যারিথমেটিকেও উভয় দিকে একই সংখ্যা দিয়ে যোগ বিয়োগ গুন করতে পারি । [ ***বিদ্রঃ উভয় দিকে একই সংখ্যা দিয়ে ভাগ করতে পারি না ।*** ]  

যেমন আমাদের রাশিটি যদি হয় $a\equiv b \text{ (mod m)}$ তাহলে কোন পূর্নসংখ্যা $k$ এর জন্য আমরা লিখতে পারি 

- $a +k\equiv b+k \text{ (mod m)}$ 

- $a-k\equiv b-k \text{ (mod m)}$

- $a\times k\equiv b\times k \text{ (mod m)}$

কেন লিখতে পারি?  নিজেরা প্রথমে প্রমাণ করার চেষ্টা কর । 

- ##### proof 1 :

  $a\equiv b \text{ (mod m)}$ হলে আমি বলতে পারি $a-b=mp$

  যেখানে `p` হল $(a-b)$ কে `m` দিয়ে ভাগ করলে যেই ভাগফল থাকবে সেইটা ( ২য় সংজ্ঞা দিয়ে চিন্তা কর) 

  এখন , 

  $a-b=mp$
  = $(a+k)-(b+k)=mp$
  তারমানে বলতে পারি , $a +k\equiv b+k \text{ (mod m)}$ 

- ##### proof 2 :

  নিজে চেষ্টা কর। 

- ##### proof 3 :

  নিজে চেষ্টা কর। 

আরও কিছু বৈশিষ্ট্য ... 

- $a \equiv b \text{ (mod m)}$ এবং $p \equiv q \text{ (mod m)}$ হলে $a+p \equiv b+q \text{ (mod m)}$
- $a \equiv b \text{ (mod m)}$ এবং $p \equiv q \text{ (mod m)}$ হলে $a-p \equiv b-q \text{ (mod m)}$
- $a \equiv b \text{ (mod m)}$ এবং $p \equiv q \text{ (mod m)}$ হলে $a\times p \equiv b\times q \text{ (mod m)}$



<div>
<details>
  <summary>stuff with *mark* **down** in `summary` doesn't work any more, use HTML <i>italics</i> and <b>bold</b> instead in <code>&lt;summary&gt;</code> (<i>click to expand</i>)</summary>
</div>
<div>`<span style="color:red">this text is red</span>`</div>

```
# A collapsible section with markdown
<details>
  <summary>Click to expand!</summary>
  
  ## Heading
  1. A numbered
  2. list
     * With some
     * Sub bullets
</details>
```

*...চলবে...*


## Reference:

- [Brilliant Wiki](https://brilliant.org/wiki/modular-arithmetic/) (আমি যখন ব্রিলিয়ান্ট উইকি খুললাম তখন অবাক হয়ে গেলাম এটা দেখে যে সংজ্ঞার অংশ দুই জায়গায় ই একই :v )
- [মডুলো অপারেশন - উইকিপিডিয়া](https://en.wikipedia.org/wiki/Modulo_operation) 