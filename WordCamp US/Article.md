# Developer takeaways from WordCamp US

Two weeks ago Taco, Patrick and I went on a trip to the US of A to visit Philadelphia for the first ever WordCamp US. There are a lot of topics to cover, but in this article I'll highlight some of my experiences as a developer taking part in WordCamp US and the WordPress Community Summit.

## Community Summit

I was honored to be invited to the Community Summit. If you don't know what it is, the [WordCamp US website][wcus] explains it very well: 

> (...) the Community Summit is a smaller, work-focused event. (...) The participant pool will be people who most actively contribute to the WordPress project.

It is also a safe space so while I won't share things we've discussed in depth, I will talk about my own experience.

### Discussion day

The topics that people proposed are publicly available on the [WordCamp US website][wcus], all topics were very interesting so it was almost impossible to choose which I wanted to participate in. Discussing important topics with fellow WordPress contributors was very enlightning and educating. It gave me new perpectives that I hadn't considered before and it really humanizes to have someone discuss their views with you.

### Working day

On the community summit working day, everyone came in, sat down and started working. It felt like everybody in that room knew how to do what they came to do. I wanted to discuss something with Taco a few times but he and the other members of the polyglot team were so concentrated that I decided to talk with him later, because I didn't want to interrupt them.

After the discussion day I really wanted to build a JavaScript parser to get JavaScript documentation into DevHub. So this is what I worked on during the working day. The only problem is that currently the JavaScript in core isn't that good. So I set up a [mirror of WordPress develop][summit-mirror] and made [Travis CI][travis] auto generate [WordPress JSDoc][summit-jsdoc].

The JS documentation is very poor, but that's because the inline documentation in WordPress is poor. I digged into the code to find out what we need to fix and prepared a make/core post containing my results and some suggestions for improvement. Because of the auto reparsing of my mirror we can easily see improvements once we improve the inline documentation.

## Session days

WordCamps are an awesome place to meet new people and to greet friends. WordCamps are just as awesome for ideas, getting new ideas or reinforcing old, lingering ones. When you start visiting WordCamps you will mainly be introduced to new ideas, but if you've been to a lot of WordCamps already most ideas will be things you have already heard before but haven't given enough thought yet.

### Introduction to WordPress unit testing

This talk by [Carl Alexander][carl-alexander] dug up an already existing idea and made it stronger. I expected this talk to be about integration testing. This is because most WordPress unit testing isn't actually unit testing. With unit testing you're testing a small unit of code to verify it works as you expect it to. Integration testing tests more parts in the code. The first time I realized this was when I watched [Ptah Dunbar's talk: Unit Testing like a Pirate][wceu-unit-testing] at the first WordCamp Europe.

Luckily for me this talk wasn't about integration testing, it was making the same point as I just did: WordPress and most WordPress plugins have integration tests but lack unit tests.

> What is unit testing? It's testing at the smallest scale. 
> 
> <cite>Carl Alexander</cite>

This is something I have been thinking about for a long time and something we also struggle with at Yoast. Currently the Yoast SEO tests take 14s on my really fast laptop and that is nothing compared to the WordPress test suite, but how long does it take for a developer to check their timeline when they are waiting?

Improving speed and consistency of our tests is something we definitely want to improve. This way we will be able to remove the WordPress dependency from our unit tests in the future.

[You can find Carl's "Introduction to WordPress unit testing" talk on wordpress.tv][wcus-unit-testing]

## Contributor day

After seeing the talk "Robots Write the Docs" by [Luke Woodward][luke-woodward], I was really inspired to start working on the parser again. When he showed up at the contributor day and wanted to work on the parser as well, I was overjoyed. He already had a [patch ready][namespace-parser-patch] to support namespaces in the parser and after some changes I merged that into the parser.

[Eric Mann][eric-mann] was working on making it possible to import JSDoc output into WordPress as post types because that is how [DevHub][devhub] works right now. The reason for custom post types is also clear to me now. I guess people want to work in WordPress since they have experience in that. In contrast to the flat HTML files that phpdocumentor and JSDoc produce, a WordPress site with posts is much more approachable for most WordPress developers.

[You can find the "Robots Write the Docs" talk on wordpress.tv][wcus-robots-docs]

## Conclusion

WordCamp US was a very productive conference where I learned a lot, met a ton of interesting people and had a lot of fun. This was the first community summit I attended and it was a blast. It really highlighted the part of the WordPress community I love: People focused. WordPress is the community.

[wcus]: https://2015.us.wordcamp.org/
[summit-mirror]: https://github.com/atimmer/wordpress-develop-mirror/
[summit-jsdoc]: http://atimmer.github.io/wordpress-jsdoc/
[wceu-unit-testing]: http://wordpress.tv/2013/12/11/ptah-dunbar-unit-testing-like-a-pirate/
[wcus-unit-testing]: http://wordpress.tv/2015/12/10/carl-alexander-introduction-to-wordpress-unit-testing/
[wcus-robots-docs]: http://wordpress.tv/2015/12/12/luke-woodward-robots-write-the-docs/
[travis]: https://travis-ci.org
[devhub]: https://developer.wordpress.org
[namespace-parser-patch]: https://github.com/WordPress/phpdoc-parser/pull/164
[carl-alexander]: https://twitter.com/twigpress
[luke-woodward]: https://twitter.com/Lkwdwrd
[eric-mann]: https://twitter.com/EricMann