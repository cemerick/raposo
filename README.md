# Raposo (Bayesian networks in Clojure)

At the second [Clojure Conj](http://clojure-conj.org), I gave a talk entitled _Modeling the world probabilistically using Bayesian networks in Clojure_.  [Video](http://blip.tv/clojure/chas-emerick-modeling-the-world-probabilistically-using-bayesian-networks-in-clojure-5961126) and [slides](https://github.com/relevance/clojure-conj/blob/master/2011-slides/cemerick-modeling-the-world-with-bayesian-networks.pdf?raw=true) from that talk are available online.  In that talk, I described and showed snippets of usage of a Bayesian network and inference library, written in Clojure, that I was wholly intending to release as an open source project very shortly after the conference.  The library's name was "Raposo" (taken from the name of the [composer of many Sesame Street songs](http://en.wikipedia.org/wiki/Joe_Raposo)…including _One of These Things (Is Not Like The Others)_, thus the connection to Bayesian inference), and I linked to [this repo](https://github.com/cemerick/raposo) as the place where the library would show up…"soon".

Many, many people have expressed an interest in using Raposo.  I'm afraid that I must finally admit that I probably will never release the library as an open source project.

As I described in the talk (or perhaps it was in the Q&A that followed, I can't remember at this point), Raposo was an attempt to distill what I learned in building and applying Bayesian nets — and in particular, building Bayesian nets in Clojure — into a resusable library that others could build upon. While the bulk of the implementation was based on working code deployed in production environments, I discovered just prior to the conference that some of the mathematics (in particular, certain integrations, although there may be additional issues I'm not yet aware of) were flawed.  Thankfully, the particular datasets that the original implementation was being applied to did not suffer from those flaws; however, other datasets _would_, and with not much work, I was able to concoct datasets that _did_.

My hope was that, after the conference, I would be able to nip and tuck the maths sufficiently to resolve the issues.  However, that never came to pass; my work and other interests ended up straying very, very far from Bayesian inference after the conference, and getting back to Raposo never quite happened.  Some have suggested that I open source the library anyway, so that others might correct my errors, use other pieces of the project, or otherwise learn from what's there.  I can't do that with a clean conscience; beyond the risk of someone using the library as-is and potentially making very bad decisions due to flawed inferences, I try very hard to not put anything out into public that I'm not proud of.  This whole episode runs counter to that, and Raposo itself certainly doesn't qualify at this point.

I feel quite bad about this, and I owe the Clojure Conj attendees and organizers in particular an apology for not following through on promises about releasing projects and code related to a conference talk.

There's a number of lessons I hope to take to heart from this; these include:

1. Never, ever, _ever_ give a talk about a library or other code publicly unless it's in a public repo prior to the talk.  Period.  (Exceptions to this might be things like case studies and such.)  Doing otherwise is surely irritating to talk attendees, but it's even more disrespectful towards organizers, as their acceptance of your talk may have been implicitly preconditioned on the attendees being able to benefit from the code/library/project in question.
2. [Shut up!](http://sivers.org/zipit); stated intentions are at best a wash in terms of motivation, and are likely actively _de_motivating.  I can't say for sure that announcing Raposo demotivated me, but I am certain that a promise to release a new open source project was never going to take priority over things like the shifting demands of "real" work, family priorities, and so on.  
3. Underpromise, overdeliver.  Timeless, but not always easy to get right.  I could just as easily presented Raposo as a case study of the awesome power of Clojure, and if/when it was ready, I could have released it.  All the win, none of the disappointment.

There's surely more, but this is long enough as it is.  I hope to come back to Raposo some day, but I don't know if or when that day will come.  If it does, code will appear here.

My apologies,

[Chas](http://cemerick.com)

(~ 2012-08-08)
