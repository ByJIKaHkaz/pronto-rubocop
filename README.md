# Pronto runner for Rubocop

[![Build Status](https://travis-ci.org/ByJIKaHkaz/pronto-rubocop.svg?branch=master)](https://travis-ci.org/ByJIKaHkaz/pronto-rubocop)
[![Gem Version](https://badge.fury.io/rb/pronto-rubocop-autocorrect.png)](https://badge.fury.io/rb/pronto-rubocop-autocorrect)

Pronto runner for [Rubocop](https://github.com/bbatsov/rubocop), ruby code analyzer. [What is Pronto?](https://github.com/mmozuras/pronto)

## Install

It's not mandatory to include gem into `Gemfile`

```
gem install pronto-rubocop-autocorrect
```

## Usage

```
pronto run -c origin/master
```

You also can ensure running before push inside `.git/hooks/pre-push`

```
pronto run -c $1/master --exit-code
```

## Configuration

Configuring Rubocop via .rubocop.yml will work just fine with pronto-rubocop.
You can also specify a custom `.rubocop.yml` location with the environment variable `RUBOCOP_CONFIG`

## How it works?

This gem patches only the modified lines in your source files. This means that the story does not deteriorate and not will happen unpleasant incidents as with rubocop -a
