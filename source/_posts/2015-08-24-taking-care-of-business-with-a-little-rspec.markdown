---
layout: post
title: "Taking Care of Business with a little RSpec"
date: 2015-08-24 00:36:00 -0400
comments: true
categories: Flatiron&nbsp;School&nbsp;Hiphop&nbsp;RSpec
---

#tldr

"Show some R-E-S-P-E-C-T for your code and your collaborators by using RSpec. For in launching RSpec, Steven Baker, Dave Astels and Aslak Hellesøy made a contribution potentially just as relevant to respectful expectations as Aretha Franklin's re-authoring techniques and Seymour Papert's vision of pioneering of creative exploration as optimal learning."

![respect_RSpec](https://raw.githubusercontent.com/rolandobrown/rolandobrown.github.io/source/source/images/RSpec_Web.png "Aretha Franklin & Seymour Papert")

#random made beautiful

This post is a creative exploration.

RSpec is a popular behaviour driven development approach that Rubyist can use to making Test-Driven Development both productive and fun.

When I first heard about "RSpec," I immediately thought about "Respect."" Not the agreement, the best practice, or the slang expression, but the song. I literally thought about the song:

  {% blockquote %}
  R-E-S-P-E-C-T
  Find out what it means to me
  R-E-S-P-E-C-T
  Take care, TCB"
  {% endblockquote %}


<iframe width="640" height="480" src="https://www.youtube.com/embed/cYbs_O_iMfU?rel=0" frameborder="0" allowfullscreen></iframe>

These words were as much as part of my upbringing as 'Wu-Tang Clan Ain't Nuthing ta Fuck Wit.' Yes, code mixing is a thing and was a thing long before our beloved Startups. Give thanks for Linguistics!

Besides it being a REMARKABLE song, sung by a REMARKABLE woman, I imagine "Respect" became a part of my superconscious as a result of it being sampled by at least 26 popular songs. As told by WhoSampled.com, 21 times by Hip-Hop & RB artists, with other songs fusing the Respect vocals with Spoken Word, Electronic/Dance and Funk tributes. Regardless of the numbers, let's just say that I have the lived experience of being programmatically injected with a notion that R-E-S-P-E-C-T was to be shown through song, rap, freestyle, humming, dancing, and other Linguistic movements.

These body of words, this bridge to be more explicit, is both an example of cultural inheritance and an instance of some larger class of cultural progression. They embody agreements that many people who love the song have efforted to bring into multiple facets of their life. I am one of these people. I'm sure many of you are also familiar with this effort.

My experience with RSpect is lightweight similar. For the scope of this post, consider RSpec a domain specific language that allows me to express a shared set of expectations for the relationships between all of my code, which, in this case, is written in a programming language named Ruby, instead of Gospel & Soul.

Ok.
Got it?
Good.

Now, I could extrapolate from these words, further abstract that right to left brain critical connection made between RSpec and Respect, into an exploration of the following:

1. RSpec
2. alternatives to RSpec like Minitest (which reminds me of safe-to-fail tests)
3. the slang expressions "Respect," "Proper Respect," or "Props"
4. my personal experience with "Respect" as a universally acceptable grassroots greeting
5. the relationship between "Respect" and "Holla"
5. other Mixin's into Hip Hop. You know: class HipHop < Roots && Soul && RB && Folk, etc.
6. the odd connections between Otis Redding, Aretha Franklin and
7. and a conversation I really need to have with Steven R. Baker about "hip hop nonsense words..."

I could. But, I won't. Because:

  ![yoda_sweetbrown](https://s-media-cache-ak0.pinimg.com/736x/ef/1e/29/ef1e29088983d6c68d96b1adea25cabd.jpg "Yoda < SweetBrown::Migrate")

What I will get into is how I internalize a good habit: Behaviour-Driven Development by using:

1. cultural foundation I luckily inherited
2. a bunch of Rspec practice labs provided by Flatiron School
2. the very reliable RSpec documentation

# But, before that a brief Historical Interlude

<script src="//repl.it/embed/BD4v/1.js"></script>

"Respect" was released by Aretha Franklin in 1967. The song was originally written by Otis Redding and released on the album: "I Never Loved A Man The Way I Love You."

Victoria Malawey, Associate Professor and Chair of the of the Music Department at Macalester College, provides a wonderful abstract:

  {% blockquote %}
  "In her re-authoring of Otis Redding's ‘Respect’, Aretha Franklin's seminal 1967 recording features striking changes to melodic content, vocal delivery, lyrics and form. Musical analysis and transcription reveal Franklin's re-authoring techniques, which relate to rhetorical strategies of motivated rewriting, talking texts and call-and-response introduced by Henry Louis Gates, Jr. The extent of her re-authoring grants her status as owner of the song and results in a new sonic experience that can be clearly related to the cultural work the song has performed over the past 45 years. Multiple social movements claimed Franklin's ‘Respect’ as their anthem, and her version more generally functioned as a song of empowerment for those who have been marginalised, resulting in the song's complex relationship with feminism. Franklin's ‘Respect’ speaks dialogically with Redding's version as an answer song that gives agency to a female perspective speaking within the language of soul music, which appealed to many audiences."
  {% endblockquote %}

Also in 1967, Seymour Aubrey Papert designed LOGO as a computer language for children. Seymour is an MIT mathematician, computer scientist, and educator. He is one of the pioneers of artificial intelligence, and co-inventor, with Wally Feurzeig, of the Logo programming language.
This might seem like a distraction but stay with me. Papert emphasized creative exploration over memorization of facts, stating:

  {% blockquote %}
  "People give lip service to learning to learn, but if you look at curriculum in schools, most of it is about dates, fractions, and science facts; very little of it is about learning. I like to think of learning as an expertise that every one of us can acquire."
  {% endblockquote %}

RSpec began life in 2005 as an experiment by Steven Baker, with early contributions from Dave Astels and Aslak Hellesøy. David Chelimsky joined the team that summer, and accepted leadership of the project in 2006. David also built rspec-rails, which provided tight integration with Ruby on Rails. Today, RSpec continues to "improve and evolve thanks to the input of a large community and the work of hundreds of contributors."

What's the critical connection between these people?

1. They inspire me
2. They value learning (i.e., "find out what it means?" "a little RSpec?" "keep on trying?")
3. They all understand something about Respect.
4. They all understand: If you want to go fast, go alone. If you want to go far, go together.
6. And don't forget about creative exploration over memorization of facts.

That's song.
That's learning.
That's programming.

- Right?
- Got it?
- Good.

So, in respect for Team RSpec, I'll be using the spelling "Behaviour," instead of "Behavior" throughout the remainder of this post.

Ok, enough exploration of music, learning and history. Let's get started.

#Getting Started

  {% blockquote %}
  "RSpec is a Behaviour-Driven Development tool for Ruby programmers. BDD is an approach to software development that combines Test-Driven Development, Domain Driven Design, and Acceptance Test-Driven Planning. RSpec helps you do the TDD part of that equation, focusing on the documentation and design aspects of TDD."" -Relish App
  {% endblockquote %}

##Install

Install RSpec and run "rspec --init" to set up your project to use RSpec. I customized by .bash_profile, so I just run they command "aretha" in order to set up my project:

{% gist b445af05173af8014ff6 %}

This installs five gems:

1. rspec
2. rspec-core
3. rspec-expectations
4. rspec-mocks
5. rspec-support

While using Rspec, run this command if you need any help:

{% gist b8049dc4db6651060455 %}

##Start Simple

Start with a very simple example that expresses some basic desired behaviour.


{% gist 9f7005381e9771ad2a1f aretha_spec.rb %}

##Fail Fast. (Video)

Run the example and watch it fail.


<iframe width="640" height="480" src="https://www.youtube.com/embed/ARcKMl_qgl8?rel=0" frameborder="0" allowfullscreen></iframe>


##Implement & Iterate

- make changes to rspec aretha_spec.rb


{% gist 5efb11808eaf783b008f aretha_spec.rb %}

Implement that basic behaviour, or those basic behaviours. Note, I recommend you build and pass one test at a time.

{% gist 1c854673544374a63158 aretha.rb %}

##Run & Refactor

Run the example and bask in the joy that is green.

$ rspec aretha_spec.rb

##Repeat, Remix, Refactor, etc.


# Expectations

**The Expect Syntax replaced The Should Syntax**

In June 2012, RSpec launched its new "Expectation Syntax."

As a result, Behaviour is now asserted by pairing expect().to and expect().not_to with a Matcher predicate. In previous versions of RSpec, the behavior assertion syntax used the keyword "should." Obviously, as one might expect, the shift from "should" to "expect" made much of RSpec's code cleaner, and unified some aspects of testing syntax.

{% gist fa12a3f7bb78cf4b75c2 shouldbe_expect.rb %}

This seems like a great shift. I imagine Programmable languages, like people, don't always respectfully return what they should. In other words, setting clear and clean expectations early in the process just... well... helps. Period.

Here're a few matchers that I found both helpful to my RSpec testing and hilariously proximate to how some of us view R-E-S-P-E-C-T in general:

- `be` matchers
- `be_within` matcher
- `satisfy` matcher
- `raise_error` matcher
- `have_attributes` matcher


**In brief, there are: **

- Equality matchers (see documentation)
- Comparison matchers (see documentation)
- Predicate matchers (see documentation)
- Type matchers (see documentation)
- Custom matchers (see documentation)


Our aretha_spec.rb RSpec test above used Type matchers. I did this in order to stay with the objects found in the song, which set a fairly straightforward set of expectations (Truthy & Falsy values). However, you can use RSpec to establish very complex and dynamic expectations, compound those expectations, aggregate failures when you have multiple independent expectations, and more.

For example, returning to the song for inspiration, what does R-E-S-P-E-C-T look like when there's no money coming home over a long period of time? Another example can be how does a couple of pair programmers engaged in a long-term collaboration engage in the generalized comparison of values? Hint: remember those comparison matchers.

##Thinking About Learning, and Learning About Thinking

Beyond what the red failures and the green successes does to our thinking, there's a way of creating. This way invites us programmers to ritually check both our assumptions and our code as we make, not after we make.

In that place, a deep understanding of RSpec Expectations lead to a very flexible safe-to-fail environment. I value flexibility as much as I value a safe-to-fail environment. Like Seymour Papert, I think we can extend this way of creating over to learning.

  {% blockquote %}
  "Many children are held back in their learning because they have a model of learning in which you have either ‘got it’ or ‘got it wrong.’ But when you program a computer you almost never get it right the first time. Learning to be a master programmer is learning to become highly skilled at isolating and correcting bugs ... The question to ask about the program is not whether it is right or wrong, but if it is fixable. If this way of looking at intellectual products were generalized to how the larger culture thinks about knowledge and its acquisition we might all be less intimidated by our fears of ‘being wrong.’ -Seymour Papert
  {% endblockquote %}

Hopefully, we can apply where appropriate some of these approaches to how we extend R-E-S-P-E-C-T in our most important relationships: the ones we have with other human beings, and, of course, our animals and plants too!


  ![hollaRSpec](https://raw.githubusercontent.com/rolandobrown/rolandobrown.github.io/source/source/images/hollaRspec.png "Steven R. Baker & Rolando Brown talk about Holla")


###Contains Samples & Inspiration from:

- [Source Code for this post on Github](https://github.com/rolandobrown/tcb)

- [RSpec Videos](http://rspec.info/)

- [RSpec Documentation](https://relishapp.com/rspec)

- [Rspec Cheat Sheet](https://www.anchor.com.au/wp-content/uploads/rspec_cheatsheet_attributed.pdf)

- [RSpec's Built-in matchers](https://www.relishapp.com/rspec/rspec-expectations/v/3-3/docs/built-in-matchers)

- [Aaron Patterson's experience with Minitest and RSpec](http://tenderlovemaking.com/2015/01/23/my-experience-with-minitest-and-rspec.html
)

- [Aretha Franklin, Respect Video](https://www.youtube.com/watch?v=cYbs_O_iMfU)

- [I Never Loved A Man The Way I Love You on Spotify](https://play.spotify.com/album/5WndWfzGwCkHzAbQXVkg2V?play=true&utm_source=open.spotify.com&utm_medium=open
)

- [‘Find out what it means to me’: Aretha Franklin's gendered re-authoring of Otis Redding's ‘Respect’. Popular Music / Volume 33 / Issue 02 / May 2014, pp 185-207Copyright © Cambridge University Press 2014](http://journals.cambridge.org/action/displayAbstract?fromPage=online&aid=9226477&fileId=S0261143014000270
)

- [Seymour Papert’s Legacy: Thinking About Learning, and Learning About Thinking](https://tltl.stanford.edu/content/seymour-papert-s-legacy-thinking-about-learning-and-learning-about-thinking)

- [Steven R. Baker and What does "holla" mean?](https://twitter.com/srbaker/status/4089813992)

- [Zoe Chodosh: Making My Bash Profile Easier and Prettier](http://zonika.github.io/blog/2015/07/30/customize-bash/)

- [Elizabeth Larcombe: LOUD IDIOT II: Parsing the Error Message](https://medium.com/@ejlarcombe/loud-idiot-ii-parsing-the-error-message-353b741b83d8?source=rss-5647f111443b------2)
