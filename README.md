<p style="padding-top: 10px;padding-bottom: 20px">
<img src="https://storage.googleapis.com/product-logos/logo_tardy.png" height="70"/>
</p>

Tardy is an easy to use, but highly configurable, CLI / terminal prompt library for Go.

[![Go Version](https://img.shields.io/badge/Go-1.4+-lightgrey.svg)](https://golang.org/)
[![Build Status](https://travis-ci.org/theyakka/tardy.svg?branch=master)](https://travis-ci.org/theyakka/tardy)
[![Coverage](https://coveralls.io/repos/github/theyakka/tardy/badge.svg?branch=master)](https://coveralls.io/github/theyakka/tardy?branch=master)
[![GoDoc](https://godoc.org/github.com/theyakka/tardy?status.svg)](http://godoc.org/github.com/theyakka/tardy)

<p>&nbsp;</p>

# Features

What can tardy do? Lots!

- Simple, straightforward prompt mechanism
- Per-prompt return values or catch-all so you can check all prompts at the end
- Built in `Prompt` types for common use-cases
  - Open-ended string values
  - Yes / No values
  - Pick from list of possible values
- Retry values that don't meet criteria or are not supplied (if not optional)
- Optionality and default prompt values
- Case sensitive (or insensitive) matching
- Extensible `Prompt` struct so you're not constrained when you need a custom input type with the following features:
  - Prompt validation function
  - Value conversion function (from string to whatever you want)

# Installing

To install, run:

```
go get -u github.com/theyakka/tardy
```

You can then import tardy using:

```
import github.com/theyakka/tardy
```

# Getting started

This is a super simple overview. If you want to really understand Tardy, we suggest you check out the [Tardy Guide](https://github.com/theyakka/tardy/wiki).

Anyhow, let's run through a super simple example.

```go
p := tardy.NewPrompter()
p.Prompt(tardy.SimplePrompt("What is your name?", tardy.Required, ""))
fmt.Println("Your name is:", p.IndexedValues[0])
```

When run, you will see a prompt. After entering a value you should see something like the following:

```
What is your name?:  John Smith
Your name is: John Smith
```


# FAQ

## Why should I use this and not ____?

Why not?

We designed this library because nothing else fit our needs. If it fits yours, cool. If not, we won't hold it against you if you use something else.

Give it a try and if you like it, let us know! Either way, we love feedback.

## Has it been tested in production? Can I use it in production?

The code here has been written based on Yakka's experiences with clients of all sizes. It has been production tested. That said, code is always evolving. We plan to keep on using it in production but we also plan to keep on improving it. If you find a bug, let us know!

# Outro

## Credits
Tardy is sponsored, owned and maintained by [Yakka LLC](https://theyakka.com). Follow us on Twitter [@yakkallc](https://twitter.com/yakkallc). Feel free to reach out with suggestions, ideas or to say hey.

### Security

If you believe you have identified a serious security vulnerability or issue with Tardy, please report it as soon as possible to apps@theyakka.com. Please refrain from posting it to the public issue tracker so that we have a chance to address it and notify everyone accordingly.

## License

Tardy is released under a modified MIT license. See LICENSE for details.

<hr/>
Tardy is a Yakka original.
<p/>
<a href="https://theyakka.com" target="_yakka">
<img src="https://storage.googleapis.com/yakka-logos/logo_wordmark.png?1234"
  width="80"></a>