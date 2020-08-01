---
title: Introduction
date: 2020-07-30 02:09:04
tags: discrete-math , math
---

মডুলার অ্যারিথমেটিক নিয়ে পড়ার আগে আমরা কিছু জিনিস রিক্যাপ করে নেই , যেগুলা আমরা ক্লাস ফাইভে পড়ে এসেছি । 

`ভাজ্য = ভাজক × ভাগফল + ভাগশেষ` বা, `Dividend = Divisor × Quotient + Remainder`

অনেকের যদি কোনটা কি জিনিস মনে না থাকে তাহলে পুরানো বইয়ের পাতা উলটে দেখতে পার , আর [গুগল](google.com) মামা তো আছেই । 

এবার অনেকর মনে প্রশ্ন আসবে , অমুক প্রবলেম তো সহজেই পাটিগণিত / সাধারণ নিয়মে সল্ভ করে  ফেলা যায় , তাহলে এসব ম্যাথ করার জন্য মডুলার অ্যারিথমেটিক কেন শিখবো? তার উপর এটা তো একটা কঠিন টপিক । 

তাদের জন্য বলে রাখা, মডুলার অ্যারিথমেটিক হল এসব সাধারণ নিয়মগুলোর একটা কম্প্যাক্ট ফর্ম । তাই এভাবে করলে সহজেই অনেক প্রবলেম সল্ভ করে ফেলা যায় । যেগুলো কিনা সাধারণ ভাবে করলে অনেক বড় হয়ে যেত ।  আর সত্যি কথা বলতে মানুষকে কোন ম্যাথের সলিউশন বুঝাতে গেলে বেশি লেখা দেখলে ভয় পেয়ে যায়। কিন্তু মডুলার অ্যারিথমেটিক দিয়ে সল্ভ করলে কয়েক লাইনে হয়ে যায় বলে তারা ভয় পায় না। (just kidding :v​ ) 



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
	{% spoiler "proof" %}
		.
    	$a\equiv b \text{ (mod m)}$ হলে আমি বলতে পারি $a-b=mp$
		যেখানে `p` হল $(a-b)$ কে `m` দিয়ে ভাগ করলে যেই ভাগফল থাকবে সেইটা ( ২য় সংজ্ঞা দিয়ে চিন্তা কর) 
		এখন , 
		$a-b=mp$
		= $(a+k)-(b+k)=mp$
		তারমানে বলতে পারি , $a +k\equiv b+k \text{ (mod m)}$ 
	{% endspoiler %}

- $a-k\equiv b-k \text{ (mod m)}$
	{% spoiler "proof" %}
	.
    নিজে চেষ্টা কর।
    {% endspoiler %}

- $a\times k\equiv b\times k \text{ (mod m)}$
	{% spoiler "proof" %}
	.
    নিজে চেষ্টা কর।
    {% endspoiler %}

আরও কিছু বৈশিষ্ট্য ... 

- $a \equiv b \text{ (mod m)}$ এবং $p \equiv q \text{ (mod m)}$ হলে $a+p \equiv b+q \text{ (mod m)}$
- $a \equiv b \text{ (mod m)}$ এবং $p \equiv q \text{ (mod m)}$ হলে $a-p \equiv b-q \text{ (mod m)}$
- $a \equiv b \text{ (mod m)}$ এবং $p \equiv q \text{ (mod m)}$ হলে $a\times p \equiv b\times q \text{ (mod m)}$



## Residue class:

কোন ধনাত্মক পূর্নসংখ্যা , $n$ দিয়ে অন্য যেকোনো পূর্নসংখ্যাকে ভাগ করলে ভাগশেষের সম্ভাব্য সকল সংখ্যাকে নিয়ে যে সেট হয় , তাকে [রেসিডিউ ক্লাস](https://artofproblemsolving.com/wiki/index.php/Residue_class) বলে ।  সহজ ভাবে বললে , কোন পূর্ন সংখ্যা , $n$ দিয়ে অন্য যেকোনো পূর্নসংখ্যাকে ভাগ করি না কেন , ভাগশেষ অবশ্যই $0$ থেকে $n-1$ এর মধ্যে হবে ( $0$ এবং $n-1$ সহ ) । যেমনঃ $5$ দিয়ে কোন সংখ্যাকে ভাগ করলে ভাগশেষ হতে পারে $\{0,1,2,3,4\}$ । তাই $5$ এর রেসিডিউ ক্লাস হল $\{0,1,2,3,4\}$ । 



## Divisibility Rule:

- $2$ **দিয়ে নিঃশেষে বিভাজ্য হওয়ার নিয়মঃ** 
  কোন সংখ্যার শেষ অংকটি যদি $2$ দিয়ে ভাগ যায় , অর্থাৎ $0,2,4,6,8$ এর মধ্যে যেকোনোটা হয় । তাহলে সংখ্যাটি $2$ দিয়ে বিভাজ্য । 
  {% spoiler "proof" %}
  .
  মনে করি সংখ্যাটি $n=10x+p$ । অর্থাৎ এর শেষ অংকটি হল $p$ । 
  তাহলে আমরা বলতে পারি , 
  $n\equiv 10x+p \text{ (mod 2)}$
  $\Longrightarrow n\equiv 0+p \text{ (mod 2)}$
  $\Longrightarrow \boxed{n\equiv p \text{ (mod 2)}}$
  অর্থাৎ $p$ ( শেষ অংক) কে $2$ দিয়ে ভাগ করলে যেই ভাগশেষ থাকবে , $n$ কে $2$ দিয়ে ভাগ করলেও একই ভাগশেষ থাকবে ।   
  {% endspoiler %}

- $3$ **দিয়ে নিঃশেষে বিভাজ্য হওয়ার নিয়মঃ**

  কোন সংখ্যার অংকগুলোর যোগফল যদি $3$ দিয়ে ভাগ যায়, তাহলে সংখ্যাটিও $3$ দিয়ে ভাগ যাবে । 
  {% spoiler "proof" %}
  .
  মনে করি সংখ্যাটি  $n=d_{0}+10d_{1}+100d_{2}+...+10^{k-1}d_{k-1}$ 

  সংক্ষেপে বললে , $n=\sum_{i=0}^{k-1}{10^{i}d_{i}}$ 
  এখানে $n$ হল $k$ অংকের একটি সংখ্যা , এবং এর অংকগুলো হল , $d_{0},d_{1},d_{2},...,d_{k-1}$। যেখানে $d_{0}$ হল একক স্থানীয় অংক, $d_{1}$ হল দশক স্থানীয় অংক , ... । 
  এখন , $10^p\equiv10\times 10 \times ... \times 10 \text{ (mod 3)}$ [মোট $p$ সংখ্যক $10$] 
  $\Longrightarrow 10^{p}\equiv 1\times 1\times 1 \times ... \times 1 \text{ (mod 3)} \equiv 1 \text{ (mod 3)}$

  অর্থাৎ , $n\equiv d_{0}+10d_{1}+100d_{2}+...+10^{k-1}d_{k-1}\text{ (mod 3)}$
  $\Longrightarrow \boxed{n\equiv d_{0}+d_{1}+d_{2}+...+10d_{k-1} \text{ (mod 3)}}$

  {% endspoiler %}

- ... 



## Problems:

- $16017020$ কে $4$ দিয়ে ভাগ করলে ভাগশেষ কত থাকবে ? 
  **সোর্সঃ BDMO regional 2018**
  {% spoiler "hint" %}

  .
  বিভাজ্যতার নিয়ম 

  {% endspoiler %}
- পরপর চারটি সংখ্যার যোগফলকে $4$ দিয়ে ভাগ করলে ভাগশেষ কত হবে ? 
  **সোর্সঃ BDMO regional 2016**
  {% spoiler "hint" %}

  .
  কবুতরের খোপের নীতি(pigeonhole principle) + Residue class

  {% endspoiler %}
- দুইটি সংখ্যার যোগফল $12$ দিয়ে বিভাজ্য । সংখ্যা দুইটির বিয়োগফলকে $2$ দিয়ে ভাগ করলে ভাগশেষ কত থাকে?
  **সোর্সঃ BDMO regional 2018**
  {% spoiler "solution" %}

  .
  মনে করি সংখ্যা দুইটি হল $a$ এবং $b$। 
  অর্থাৎ $a+b\equiv 0 \text{ (mod 12)}$
  $\Longrightarrow a+b = 12k$
  $\Longrightarrow a-b = 12k-2b$
  $\Longrightarrow a-b = 2(6k-b)$
  $\Longrightarrow a-b \equiv 2(6k-b) \text{ (mod 2)}$
  $\Longrightarrow \boxed{a-b \equiv 0 \text{ (mod 2)}}$
  {% endspoiler %}

- $11+12+13+14.....+2019= S$
  What will be the remainder when dived by $100$?
  {% spoiler "solution" %}

  .
  $s=(1+2+3+...+2019)-(1+2+3+...+10)$
  $s=\frac{2019\times 2020}{2}-\frac{10\times 11}{2}$
  $s=2019\times 1010-5\times 11$
  $s \equiv 2019\times 1010-5\times 11 \text{ (mod 100)}$
  $s \equiv 19\times 10-5\times 11 \text{ (mod 100)}$
  $s \equiv 190-55 \text{ (mod 100)}$
  $s \equiv 135 \text{ (mod 100)}$
  $s \equiv \boxed{35} \text{ (mod 100)}$
  {% endspoiler %}
- $s=2016-2015+2014-2013+...+4-3+2-1$
  $s$ কে $4$ দিয়ে ভাগ করলে ভাগশেষ কত হবে ? 
  **সোর্সঃ BDMO regional 2018**
  {% spoiler "hint" %}

  .
  পরপর দুইটি সংখ্যা নিয়ে জোড়া করে হিসাব করলেই হয়ে যায় । এই সমস্যায় মডুলার অ্যারিথমেটিক তেমন কোন কাজে লাগে না । 
  {% endspoiler %}
- $s=2^{2}+4^{2}+8^{2}+...+512^{2}+1024^{2}$
  $s$ এর শেষ অংক কত? 
  **সোর্সঃ BDMO regional 2016**
  {% spoiler "hint" %}

  .
  এখানে আসলে আমাদের $s \text{ (mod 10)}$ বের করতে হবে । 
  আমাদের পদগুলোর সাধরন রূপ হল $2^(2x)$ [যেখানে $x\ge 1$ এবং $x$ পূর্ন সংখ্যা]
  $2^{2x}=2^{2(x-1)+2}=2^{2(x-1)}\times 2^{2}=2^{2(x-1)}\times 4$
  অর্থাৎ , কোন পদের মডুলো মান হবে তার আগের মডুলো মানের $4$ গুন । 
  প্রথম পদ , $2^2\equiv 4 \text{ (mod 10)}$
  দ্বিতীয় পদ , $2^4\equiv 4 \times 4 \equiv 6 \text{ (mod 10)}$
  তৃতীয় পদ , $2^6\equiv 6 \times 4 \equiv 4 \text{ (mod 10)}$
  ...
  এভাবে $4$ আর $6$ আস্তে থাকবে চক্রাকারে । এখান থেকে পরপর দুইটি পদ নিয়ে হিসাব করলেই হয়ে যাবে । 
  {% endspoiler %}
- একটি গোল টেবিলে $10$ টি চেয়ারে দশজন লোক বসে আছে । চেয়ারগুলো ঘড়ির কাটার ঘুর্ননের দিকে $0,1,2,...,9$ সংখ্যা দিয়ে ক্রমানুসারে চিহ্নিত করা । $0$ চিহ্নিত চেয়ারে থাকা লোকটির কাছে একটি বল আছে এবং বলটিকে এখন ঘড়ির কাটার ঘূর্ননের দিকে একজনের কাছে থেকে অপরজনের কাছে পাঠানো হবে । প্রথম ধাপে বলটি $1^{1}$ সংখ্যক চেয়ার ঘুরে $1$ চিহ্নিত চেয়ারে যায় । দ্বিতীয় ধাপে সেখান থেকে আরও $2^{2}$ সংখ্যক চেয়ার ঘুরে $5$ চিহ্নিত চেয়ারে যায় । তৃতীয় ধাপে বলটি সেখান থেকে আরও $3^{3}$ সংখ্যক চেয়ার ঘুরে $2$ চিহ্নিত চেয়ারে যায় । এভাবে $2020$ তম ধাপে বলটি কত নাম্বার চেয়ারে থাকবে ? 
  **সোর্সঃ BDMO regional 2017**
  {% spoiler "hint" %}

  .
  এখানে আসলে আমাদের $\sum_{i=1}^{2020}{i^i} \text{ (mod 10)}$ বের করতে হবে ।
  সহজ ভাষায় $1^1+2^2+3^+...+2020^{2020} \text{ (mod 10)}$  বের করতে হবে ।
  চক্র(cycle) বের করে সহজেই এই সমস্যাটির সমাধান করা যায় ।  
  {% endspoiler %}
- $c=2^{1}+2^{2}+2^{3}+2^{4}+...+2^{2017}+2^{2018}$
  $c$ কে $3$ দিয়ে ভাগ করলে ভাগশেষ কত থাকবে ? 
  **সোর্সঃ BDMO regional 2018** 
  {% spoiler "hint" %}

  .
  $a^p \text{ (mod m)}$ এরকম আকারের যেকোনো সংখ্যার একটি বৈশিষ্ট্য হল $a,m$ এর ফিক্স মানের জন্য $p$ এর মান বাড়ালে চক্র(cycle) পাওয়া যায়।  
  এই সমস্যার ক্ষেত্রে আমরা $2,1,2,1,...$ এরকম চক্র পাবো , এখান থেকে পরপর দুইটি মানের জোড়া নিয়ে হিসাব করলেই হয়ে যাবে । 
  এই সমস্যাটি গুণোত্তর ধারা (geometric series) +  মডুলার অ্যারিথমেটিক দিয়েও করা যায় । 
  {% endspoiler %}
- A = 1234...............100 (Using all number from 1 to 100 conjecutively) What will be the remainder if A is divide by 9?
  **সোর্সঃ KUET math club , mothly challenge - 1**
  {% spoiler "solution" %}

  .
  **Bonus question**:  If we concatenate n number ($a_1,a_2,a_3,...a_n$). And thus get number `M` then prove that $M\equiv \sum_{i=1}^{n}{a_i}\text{ (mod 9)}$  

  **proof** : 

  if the length of the $i_{th}$ number is $p_{i}$ then we can write,

  $M=\sum_{i=1}^{n}{a_{i}\times 10^{\sum_{j=i+1}^{n}{p_{j}}}}$

  in short we can write , $M=\sum_{i=1}^{n}{10^{x_i}a_i}$ 

  where, $x_i = \sum_{j=i+1}^{n}{p_{j}}$

  as $10^x\equiv 1 \text{ (mod 9)}$

  hence , $10^x a\equiv a \text{ (mod 9)}$

  $\therefore M\equiv\sum_{i=1}^{n}{10^{x_i}a_i}\equiv\sum_{i=1}^{n}{a_i} \text{ (mod 9)}$ 

  

  Now in this problem we can say that $A\equiv\sum_{i=1}^{100}{i} \text{ (mod 9)}$

  $\Longrightarrow A\equiv 100 \text{ (mod 9)}$ [as $\sum_{i=1}^{99}{i} \equiv 0 \text{ (mod 9)}$]

  $\Longrightarrow A\equiv \textcolor{red}{\boxed{1}} \text{ (mod 9)}$

  {% endspoiler %}
- $122333444455555666666...10000000001000000000...1000000000$ কে $3$ দিয়ে ভাগ করলে ভাগশেষ কত থাকবে? 
  **সোর্সঃ BDMO regional 2015**
  {% spoiler "hint" %}

  .
  
  আগের সমস্যার সমাধান দেখে নিজে চেষ্টা করো । 

  {% endspoiler %}

অনেক হয়ে গেলো শুধুমাত্র ম্যাথ নিয়ে সমস্যা । এখন কিছু প্রোগ্রামিং নিয়েও সমস্যা দেখা যাক । 

- আমাদের $3$ টা পূর্নসংখ্যা দেওয়া আছে $p,q,m$ যেখানে $0\le p,q \le 10^9$ এবং $1\le m \le 10^9$ । আমাদেরকে $pq \text{ (mod m)}$ এর মান প্রিন্ট করতে হবে । 
  {% spoiler "hint" %}

  .
  
  $p,q$ যেহেতু $10^9$ পর্যন্ত হতে পারে , তাই এদের গুণফল $10^{18}$ পর্যন্ত হয়ে যেতে পারে । তাই এই ভ্যারিয়েবল গুলো `long long` টাইপের নিতে তবে ( অথবা `long long` এ টাইপকাস্ট করে নিতে হবে )
  {% endspoiler %}
  {% spoiler "code" %}

  .
  
  {% vimhl cpp true %}
  #include <stdio.h>
  int main() {
    long long p, q;
    int m;
    scanf("%lld %lld %d", &p, &q, &m);
    printf("%lld\n", (p * q) % m);
    return 0;
  }
  {% endvimhl %}
  {% endspoiler %}
- এখন আগের প্রবলেমেই রেঞ্জটা একটু চেঞ্জ করে দিলে কেমন হয়? $0\le p,q \le 10^{18}$ এবং $1\le m \le 10^9$
  {% spoiler "hint" %}

  .
  
  $p,q$ যেহেতু $10^{18}$ পর্যন্ত হতে পারে , তাই এটি আগের পদ্ধতিতে সল্ভ করা যাবে না , কাড়ন  এদের গুণফল $10^{36}$ পর্যন্ত হয়ে যেতে পারে এবং এই রেঞ্জের কোন ভ্যারিয়েবল c++ এ নাই।
  যদি $p\equiv a \text{ (mod m)}$ এবং $q\equiv b \text{ (mod m)}$ হয় , তাহলে আমরা বলতে পারি $pq\equiv ab \text{ (mod m)} \Longrightarrow pq\equiv \{(p\text{ (mod m)})\times(q\text{ (mod m)})\} \text{ (mod m)}$
  {% endspoiler %}
  {% spoiler "code" %}
  .
  {% vimhl cpp true %}
  int main() {
    long long p, q;
    int m;
    scanf("%lld %lld %d", &p, &q, &m);
    p%=m;
    q%=m;
    printf("%lld\n", (p * q) % m);
    return 0;
  }
  {% endvimhl %}
  {% endspoiler %}
- **Russian Multiplication System** :
- **Big Integer Modulo** : 

 *...চলবে...*


## Reference:

- [Brilliant Wiki](https://brilliant.org/wiki/modular-arithmetic/) (আমি যখন ব্রিলিয়ান্ট উইকি খুললাম তখন অবাক হয়ে গেলাম এটা দেখে যে সংজ্ঞার অংশ দুই জায়গায় ই একই :v )
- [মডুলো অপারেশন - উইকিপিডিয়া](https://en.wikipedia.org/wiki/Modulo_operation) 
- [Divisibility rule from wiki](https://en.wikipedia.org/wiki/Divisibility_rule)
- [Some Misconception about modulo](https://brilliant.org/wiki/modular-arithmetic-misconceptions/)

