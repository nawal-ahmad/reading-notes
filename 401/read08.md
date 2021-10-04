# Read: 08 - OO Design

## Don’t repeat yourself (DRY):

> It is a principle of software development aimed care about reducing repetition of software patterns, replacing it with abstractions or using data normalization to avoid redundancy.

> The DRY principle is stated as "Every piece of knowledge must have a single, unambiguous, authoritative representation within a system".
When the DRY principle is applied successfully, a modification of any single element of a system does not require a change in other logically unrelated elements.

## Alternatives:
1. WET: Commonly taken to stand for write `everything twice` WET used when a developer may be tasked with, for example, adding a comment field on a form in a web application.

A DRY approach eliminates that redundancy by using frameworks that reduce or eliminate all those editing tasks except the most important ones.

2. AHA: stands for `Avoid Hasty Abstractions` is rooted in the understanding that the deeper the investment we've made into abstracting a piece of software, the more we perceive that the cost of that investment can never be recovered, AHA programming assumes that both WET and DRY solutions inevitably create software that is rigid and difficult to maintain. 

## Rule Of Three:
Rule of three `Three strikes and you refactor` is a code refactoring rule of thumb to decide when similar pieces of code should be refactored to avoid duplication. It states that two instances of similar code do not require refactoring, but when similar code is used three times, it should be extracted into a new procedure. =

**Duplication** is considered as a bad practice in programming because it makes the code harder to maintain. When the rule encoded in a replicated piece of code changes, whoever maintains the code will have to change it in all places correctly.

## You aren't gonna need it:
**YAGNI** is a principle of extreme programming that states a programmer should not add functionality until deemed necessary.

YAGNI is a principle behind the XP practice of `do the simplest thing that could possibly work.`  It is meant to be used in combination with several other practices, such as continuous refactoring, continuous automated unit testing, and continuous integration. Used without continuous refactoring.

## minimum viable product (MVP):
A minimum viable product (MVP) is a version of a product with just enough features to be usable by early customers who can then provide feedback for future product development.

Developers potentially avoid lengthy and (ultimately) unnecessary work. Instead, they iterate on working versions and respond to feedback, challenging and validating assumptions about a product's requirements.

