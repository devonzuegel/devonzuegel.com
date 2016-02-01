---
title: 'Projects'
tags: []
collection: pages
---

## TiddlyLisp ##
###### <div class='time'>January 2016</div><br> ######

To learn the fundamentals of Lisp, I built a little interpreter based on Michael Nielsen's fantastic blog post [*Lisp as the Maxwell's Equations of Software*](http://www.michaelnielsen.org/ddi/lisp-as-the-maxwells-equations-of-software/). I included extensions to resolve some of the challenge problems he mentioned at the end of the post, too.

You can find the code for the interpreter on [Github](//github.com/devonzuegel/tiddly-lisp).

## Instanote ##
###### <div class='time'>January 2016</div><br> ######

About a month ago, I started using Instapaper obsessively. However, it left me with one major problem –– all of my Instapaper bookmarks and highlights were isolated from the knowledge that I (obsessively) store in Evernote, and I wanted to have them all in one place. After all, a [personal knowledge base](https://en.wikipedia.org/wiki/Personal_knowledge_base) is useless if it doesn't contain half of the things I read throughout the day.

Instanote solves this problem by syncing the text of my archived Instapaper bookmarks with their respective highlights into Evernote every 10 minutes. I figured other people might have the same frustration with Instapaper, so I built out a little Heroku app that allows other people to sign up too rather than just hard-coding my login info into a hacky script.

You can sign up at [instanote-archive.herokuapp.com](https://instanote-archive.herokuapp.com) and see the source code on [Github](https://github.com/devonzuegel/instanote-archive).

## Congressional Bill Outcome Predictor ##

###### <div class='time'>December 2015</div><br> ######

Emma Marriott, Arushi Jain, and I built a predictor that identifies which US bills will succeed in the House & Senate. We tried several different prediction methods, including: Naive Bayes with and without Principal Component Analysis (PCA), Logistic Regression, Support Vector Machine (SVM) with PCA, and Perceptron with PCA. PCA identified the `500` most important features of a set of `11,000`. Each predictor was modeled on data from the 109th – 113th Congresses from a wide range of structured & unstructured sources, including lobbying information. SVM with PCA proved to be the best model. It predicted bill outcomes with `94%` precision & `87%` recall, resulting in an F-measure of `0.92`.

You can learn more about our research and data [here](http://devonzuegel.com/bills/).

## Affitto ##

###### <div class='time'>November 2015</div><br> ######

San Francisco and the greater Bay Area have been struggling with housing shortages and decisions about how to best serve the community with policies to deal with this situation. At a micro level, we have a fairly good understanding of how individuals make economic decisions such as where tenants choose to live and how much rent landlords choose to charge. However, we lack tools to model the complex interactions of millions of individuals simultaneously making decisions and the emergent phenomena that result from these interactions.

John Luttig and I built an Agent Based Model (ABM) to simulate emergent behavior within housing markets and explore the impact of policies such as rent control and zoning regulations. With this project, we aim to provide a tool for policymakers and stakeholders to better understand these interactions that in aggregate comprise the housing market. Understanding large-scale systems requires understanding how the results of individual actions can be more than the sum of its parts. We used ABM to simulate the actions and interactions of tenants and landlords.

Here is a small version of one of our models. You may have to close the controls (by clicking the bottom of the control panel) in order to see the full simulation.

<iframe src='http://htmlpreview.github.io/?https://raw.githubusercontent.com/devonzuegel/affitto/blob/master/models/model2-small/model.html' style='width:100%; height: 390px;' frameborder='no' border='0'></iframe>

You can find the ABM code, housing data with which we initialized the model, and further information on the analysis we performed on the resulting network at [github.com/devonzuegel/affitto](//github.com/devonzuegel/affitto). You can see a larger version of the model [here](http://htmlpreview.github.io/?https://raw.githubusercontent.com/devonzuegel/affitto/blob/master/models/model2/model.html).

## My Evernote ##
###### <div class='time'>July 2015</div><br> ######

I love Evernote. On any given day I usually create about 15 notes, ranging from highlighted blog posts and articles to trip itineraries and to-do lists. The bulk of these notes are clippings from around the web that I've read and annotated with Evernote's [Clearly extension](//evernote.com/clearly/).

Evernote has lots of great sharing capabilities, including joint notebooks, public links, and social sharing. However, I've always wanted to publish a sort of feed that shares a select set from my annotated notes and displays what my friends have read. What I want is a bit like Medium, but where the posts aren't necessarily from that platform, simply clipped with Evernote into a notebook.

As a fun way to solve this little problem of mine and to teach myself more about Rails testing frameworks, I'm working on a little app called [My Evernote](//myevernote.co). When I'm done, it'll automatically sync all of your notes except those you especially tag `#private`. Then each evening you receive an email asking which of the synced notes you want to "publish" on your feed. It's a simple app, but I quickly learned that the Evernote documentation for Rails is basically non-existent, so it's also been a fun way to add to that.

![](../assets/my-evernote.png)

You can find the open source code for the project on [Github](//github.com/devonzuegel/my-evernote) and the app at [myevernote.co](//myevernote.co).

## Zen Writer ##
###### <div class='time'>June 2015</div><br> ######

The most difficult part of writing is that first draft. Putting your ideas to paper to generate that initial content is hard, because it's natural to edit your thoughts while translating them into words. However, this can severely hamper progress and creativity during early drafts. I've learned that I write better content faster if I don't censor myself initially and then only allow myself to revise and edit after I've exhausted my ideas. However, it's extremely difficult to contain that urge to filter out the less well-formed ideas.

During spring quarter finals, I was assigned a 10 page paper. Just three days before it was due I had a one page draft despite hours of research and staring at a blank screen. I had lots of ideas in my head, but every time I started typing I ended up using the delete button almost as much as all my other keys combined.

Since I wasn't making any progress anyways, I decided to take a break and built a tiny text editor called [Zen Writer](//zenwriter.io). It disables the delete button, highlights the current line, and fades out past content so that your attention is focused on moving forward and generating more content.

It didn't take much work to build a rough version, and as soon as I finished I was back to writing that first draft of my paper. In the first 15 minutes, I generated about 600 words. When I went back to revise what I'd written, I was surprised to find that most of my changes were to fix minor typos rather than large, conceptual revisions.

I finished that first draft in just over 2 hours and spent another hour the following day to revise my work, and the resulting paper was among the best I've written in my time at Stanford. Since then, I use Zen Writer every time I get stuck writing, from emails to blog posts to READMEs. I hope other people find it useful too, though I will warn you that it's still very rough and simple!

You can find the open source code for the project on [Github](//github.com/devonzuegel/zen-writer) and the app at [zenwriter.io](//zenwriter.io).

## OrigamiJS ##
###### <div class='time'>March 2015</div><br> ######

Over spring break I decided I wanted to play around with coffeescript, so I built a little script to hierarchically fold elements on a webpage. I originally built it so I could fold long blog posts and class notes I had written in Markdown. The idea was inspired by the great header folding in [Marked2](http://marked2app.com/), my favorite Markdown previewer, so by default Origamijs folds traditional `<h*>` and `<p>` elements as defined by Markdown. Origamijs also allows clients to define their own hierarchy, in the case that they're using unique tags or prefer to ignore certain levels of the traditional Markdown tag hierarchy.

You can find the open source code for the project on [Github](//github.com/devonzuegel/origamijs) and example usage [here](//htmlpreview.github.io/?https://raw.githubusercontent.com/devonzuegel/origamijs/master/example-coffee.html).

## Fiesta: Machine Translator ##
###### <div class='time'>March 2015</div><br> ######

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
###### <div class='time'>Summer 2014</div><br> ######

![right-sm](http://michaelandassociate.com/fifteen/wp-content/uploads/2014/11/formation8.jpg)

This past summer, I designed and built an app called Octagon, a tool for venture capital firms. Octagon helps VCs better manage relationships with portfolio companies by visualizing important metrics about company growth and providing a repository for financial documents and quarterly updates. It also facilitates interaction between investors and board members and the startups in their portfolios in an analogous manner to CRM software. Octagon is currently in beta testing at Formation|8.

I was responsible for the full-stack of the app, though I was lucky enough for the last few weeks of the project to work with a friend named Zack who helped me immensely with the front-end, especially user interaction and fully utilizing the capabilities of our graphing libraries.

You can find the open source code for the project on [Github](//github.com/devonzuegel/octagon).

## Paper Trail ##
###### <div class='time'>March 2014 - present</div><br> ######

Some of the greatest impact individuals can have on politics is driven by daily purchasing decisions. Any time an individual patronizes a corporation, (s)he is fueling the company's lobbying and donorship capabilities and is indirectly supporting their political causes. Unfortunately, the impact of corporate political contributions is largely opaque to the general public, and the research about corporations’ political activity is a tedious, complex task.

In early 2014, I set out to solve this problem with a project called Paper Trail. The web app provides users access to political profiles of companies and manufacturers. Visualizations and statistics about companies political contributions and lobbying behavior help consumers make informed choices about where their money is going. In turn, consumers' more thoughtful choices empower those corporations that represent their values.

Paper Trail was the first programming project that I pursued outside of class and has evolved significantly since I first implemented it in early 2014. It began as a simple HTML/Javascript app into which users could query the names of companies and learn about their political contributions.

You can find this initial prototype [here](//stanford.edu/~devonz/paper_trail/about.html) and the open source code base on [Github](//github.com/devonzuegel/WWW/tree/master/paper_trail).

Last month, I decided to completely refactor and improve upon Paper Trail with the help of a few friends. We realized that it was unlikely that users would consistently use the app alongside real-life spending, because it would require the tedious process of pulling their phone out of their pocket, typing in the company name, and analyzing the results. We had to find a way to integrate Paper Trail more seamlessly into the users' existing workflow.

We decided that a browser extension would be far more effective than the original idea of a standalone website. Our extension lies on top of Amazon and automatically alerts users of the political activities of the manufacturers of the items in the user's cart. Beyond solving the problem of relying on users to take action, our new strategy also narrowed our focus to a single site — Amazon — and its users. This had the benefit of leveraging our own experience as Amazon customers, using Amazon's fantastic API, and generally focusing our energy on specific goals rather than broad ones. 

The Paper Trail extension is currently under development. You can find an rough interactive prototype on [Invision](//invis.io/SZ1M1F6AJ) and the open source code for the actual extension on [Github](//github.com/devonzuegel/papertrail-extension).

## In Other Words ##
###### <div class='time'>January - May 2011</div><br> ######

![right-md](http://bookshow.blurb.com/bookshow/cache/P2866696/md/cover_2.jpeg)

My brother Jeffrey was born with Cerebral Palsy and is on the autistic spectrum. Life with Jeffrey is challenging for both of us because he doesn’t always communicate effectively in the conventional way, in “English.” However, he has found alternative modes with the help of his team of teachers, therapists, family, and friends.

In my junior year in high school, I became fascinated with his growing ability to communicate in non-conventional ways and decided to devote several months to learning more about this process. After conducting extensive interviews and reading further into psychology and cognitive science, I published a documentary book called In Other Words about how he and his team discovers and develops those alternatives.

You can find the book on [Blurb.com](http://www.blurb.com/b/2092327-in-other-words).