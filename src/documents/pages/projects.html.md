---
title: 'Projects'
tags: []
collection: pages
---

## Fiesta: Machine Translator ##
###### <div class='time'>March 2015</div><br>

Zoe Robert, John Luttig, and I built a Spanish to English machine translator, which we called Fiesta. It is based on the IBM Model 1 algorithm and also implements several Spanish-specific strategies for improving results.

IBM Model 1 is an **expectation-maximization statistical alignment algorithm**. Given known pairings of Spanish and English sentences, it generates a matrix of probabilities whose rows correspond to the Spanish vocabulary and columns correspond to the English vocabulary. The value at any given cell in the matrix represents the probability that those two words have co-occurred within translations of each other. This table is then used to estimate a model for future translations.

In short, IBM Model 1 looks for the most likely English word for a Spanish word (e.g. “dog”) based off our knowledge of co-occurrences within sentences. As such, if there are no translations of a given Spanish word `s` that contain a given English word `e`, the value of the cell at the corresponding row and column will be `0`.

The algorithm requires 3 components:

- a language model to compute `P(E)` (the prior)
- a translation model to compute `P(S|E)` (the probability that a Spanish word `s` translates to an English word `e`)
- a decoder that produces the most probable translation

#### Pseudocode ####

```python
initialize transl_prob(e|s) uniformly
do until convergence
  set count(e|s) to 0 for all e,s
  set total_s(s) to 0 for all s
  for all sentence pairs (en_sentence, sp_sentence)
    set total_e(e) = 0 for all e
    for all words e in en_sentence
      for all words s in sp_sentence
        total_e(e) += transl_prob(e|s)
    for all words e in en_sentence
      for all words s in sp_sentence
        count(e|s) += transl_prob(e|s) / total_e(e)
        total_s(s) += transl_prob(e|s) / total_e(e)
  for all s
    for all e
      transl_prob(e|s) = count(e|s) / total_s(s)
```

You can find the open source code for the project on [Github](//github.com/devonzuegel/fiesta).

## Octagon ##
###### <div class='time'>Summer 2014</div><br>

![right-sm](http://collectivehealth.com/wp-content/uploads/2014/08/formation-8-logo-700x192.png)

This past summer, I designed and built an app called Octagon, a tool for venture capital firms. Octagon helps VCs better manage relationships with portfolio companies by visualizing important metrics about company growth and providing a repository for financial documents and quarterly updates. It also facilitates interaction between investors and board members and the startups in their portfolios in an analogous manner to CRM software. Octagon is currently in beta testing at Formation|8.

I was responsible for the full-stack of the app, though I was lucky enough for the last few weeks of the project to work with a friend named Zack who helped me immensely with the front-end, especially user interaction and fully utilizing the capabilities of our graphing libraries.

You can find the open source code for the project on [Github](//github.com/devonzuegel/octagon).

## Paper Trail ##
###### <div class='time'>March 2014 - present</div><br>

Some of the greatest impact individuals can have on politics is driven by daily purchasing decisions. Any time an individual patronizes a corporation, (s)he is fueling the company's lobbying and donorship capabilities and is indirectly supporting their political causes. Unfortunately, the impact of corporate political contributions is largely opaque to the general public, and the research about corporations’ political activity is a tedious, complex task.

In early 2014, I set out to solve this problem with a project called Paper Trail. The web app provides users access to political profiles of companies and manufacturers. Visualizations and statistics about companies political contributions and lobbying behavior help consumers make informed choices about where their money is going. In turn, consumers' more thoughtful choices empower those corporations that represent their values.

Paper Trail was the first programming project that I pursued outside of class and has evolved significantly since I first implemented it in early 2014. It began as a simple HTML/Javascript app into which users could query the names of companies and learn about their political contributions.

You can find this initial prototype [here](//stanford.edu/~devonz/paper_trail/about.html) and the open source code base on [Github](//github.com/devonzuegel/WWW/tree/master/paper_trail).

Last month, I decided to completely refactor and improve upon Paper Trail with the help of a few friends. We realized that it was unlikely that users would consistently use the app alongside real-life spending, because it would require the tedious process of pulling their phone out of their pocket, typing in the company name, and analyzing the results. We had to find a way to integrate Paper Trail more seamlessly into the users' existing workflow.

We decided that a browser extension would be far more effective than the original idea of a standalone website. Our extension lies on top of Amazon and automatically alerts users of the political activities of the manufacturers of the items in the user's cart. Beyond solving the problem of relying on users to take action, our new strategy also narrowed our focus to a single site — Amazon — and its users. This had the benefit of leveraging our own experience as Amazon customers, using Amazon's fantastic API, and generally focusing our energy on specific goals rather than broad ones. 

The Paper Trail extension is currently under development. You can find an rough interactive prototype on [Invision](//invis.io/SZ1M1F6AJ) and the open source code for the actual extension on [Github](//github.com/devonzuegel/papertrail-extension).

## In Other Words ##
###### <div class='time'>January - May 2011</div><br> ######

![right-md](http://www.freestyle.mvla.net/~DevonZ/project3/images/photo1.JPG)

My brother Jeffrey was born with Cerebral Palsy and is on the autistic spectrum. Life with Jeffrey is challenging for both of us because he doesn’t always communicate effectively in the conventional way, in “English.” However, he has found alternative modes with the help of his team of teachers, therapists, family, and friends.

In my junior year in high school, I became fascinated with his growing ability to communicate in non-conventional ways and decided to devote several months to learning more about this process. After conducting extensive interviews and reading further into psychology and cognitive science, I published a documentary book called In Other Words about how he and his team discovers and develops those alternatives.

You can find the book on [Blurb.com](http://www.blurb.com/b/2092327-in-other-words).