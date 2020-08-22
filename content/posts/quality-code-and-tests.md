---
title: "Quality Code and Tests"
date: 2020-08-14T20:09:58+02:00
draft: false
---

Recently I've seen a codebase in which the technical manager told the
developers the importance of having tests. And one of the goals of the
company for the following months was to increment the code coverage.

The codebase had 10 years and was not created to be testable in mind and
without following any good practice. There was a lack of use of SOLID
principles, there was no documented architecture, ... When the
developers started to add tests they had to create mocks. For most of
the tests, they had many lines of mocks setup and it was really
difficult to understand what behaviour was under the test. In fact, the
test was testing the implementation, not the behaviour.

Many times if there was a change in the result of the code under test,
the test would still be green. Opposite, if there was a change in the
implementation of the code, the test would change to red, even if the
result was the same. That should tell us something about how we do
tests.

When I explore the codebase I was really scared to change anything
because I didn't have a way to know if something broke with my change. I
didn't believe the tests. Nobody wanted to do any refactor for the same
reasons.

In my opinion, if a test is stopping you to refactor the code, you would
change the test and the code under test as soon as possible. If not, the
technical debt will grow to a point where any change will be dangerous.
Consequently, the product will be stalled.

As a conclusion, I would say that you should not care about the coverage
percentage. You should care about if the tests are given you the
confidence that the code is working.

