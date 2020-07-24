# Gungnir

A high level, data driven database library for Clojure data mapping.

[![Build Status](https://travis-ci.org/kwrooijen/gungnir.svg?branch=master)](https://travis-ci.org/kwrooijen/gungnir)
[![codecov](https://codecov.io/gh/kwrooijen/gungnir/branch/master/graph/badge.svg)](https://codecov.io/gh/kwrooijen/gungnir)
[![Dependencies Status](https://versions.deps.co/kwrooijen/gungnir/status.svg)](https://versions.deps.co/kwrooijen/gungnir)
[![Clojars Project](https://img.shields.io/clojars/v/gungnir.svg)](https://clojars.org/kwrooijen/gungnir)
[![Slack](https://img.shields.io/badge/clojurians-gungnir-blue.svg?logo=slack)](https://clojurians.slack.com/messages/gungnir/)

> It is said that Gungnir could strike any target, regardless of the wielder's
> skill.
>
> -- Developer, speaking to the database admin.

[Read the guide](https://kwrooijen.github.io/gungnir/guide.html)

## Rationale

### Plug & Play setup

The Clojure community tends to lean towards the "pick the libraries that you
need" method rather than using a "framework" when building an application. Which
can make it challenging for new users. Once you're familiar with the Clojure
ecosystem you'll know which libraries you prefer and create your own setup. And
that's exactly what I've done.

If you want complete control over your database stack, then this is probably not
for you. If you're a beginner and are overwhelmed with all the necessary
libraries and configuration, or if you're looking for a Clojure database library
that aims to provide a quality of life experience similar to Ruby's ActiveRecord
or Elixir's Ecto, then stick around.

### Data Driven

I cannot stress this enough, I really dislike macros. Clojure and a large part
of its community have taught me the beauty of writing data driven code. With
libraries such as HoneySQL, Hiccup, Integrant, Reitit, Malli, I think this is
the Golden age of Data Driven Clojure. I never want to see macros in my API
again.

## Features

### Plug & Play™

Include Gungnir in your project, and off you go! Gungnir includes (almost)
everything you need for your app.

* [next-jdbc](https://github.com/seancorfield/next-jdbc)
* [hikari-cp](https://github.com/brettwooldridge/HikariCP)
* [HoneySQL](https://github.com/seancorfield/honeysql)
* [Malli](https://github.com/metosin/malli)
* TODO - Create a data driven migration library

### Models

Gungnir uses models to provide data validation and seamless translation between
Clojure and SQL. [Read more](https://kwrooijen.github.io/gungnir/model.html)

### Changesets

Inspired by Elixir Ecto's Changesets. Validating your data before creating and
updating it in the database. View the actual changes being made, and aggregate
any error messages. [Read
more](https://kwrooijen.github.io/gungnir/changeset.html)

### Querying & Extension to HoneySQL

Gungnir isn't here to reinvent the wheel. Even though we have an interface for
querying the database, we can still make use of HoneySQL syntax. This allows us
to expand our queries, or write more complex ones for the edge cases. [Read
more](https://kwrooijen.github.io/gungnir/query.html)

### Relational mapping

Relations are easily accessed with Gungnir. Records with relations will have
access to `relational atoms` which can be dereffed to query any related
rows. [Read
more](https://kwrooijen.github.io/gungnir/model.html#model-relation-definitions),
[and more](https://kwrooijen.github.io/gungnir/query.html#querying-relations)


## Resources

### Guide

### Code Playground

## Author / License

Released under the [MIT License] by [Kevin William van Rooijen].

[Kevin William van Rooijen]: https://twitter.com/kwrooijen

[MIT License]: https://github.com/kwrooijen/gungnir/blob/master/LICENSE
