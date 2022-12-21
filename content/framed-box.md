+++
title = "How to create a framed box"
date = "2022-12-21"
author = "Radek"
type = "page"
+++

I have got lots of recuring questions about the framed box on the demo website, so I finally wrote it down.

So there was an idea: I wanted to put some "hello / welcome" note before the list of the posts on the demo page and I wanted it to be simple.

I came up with idea to use the usually empty `_index` files in Hugo. These files allow you to create the list of contents, but what if I want to put something dynamically before / around / after the list itself? I thought — just take the `.Content` variable and use it inside the list template to style it. That was it!

Here is a list of steps you need to do to re-create it:

1. inside your `_index.{md|html}` file, add a param called `framed` with a value of `true` (something like that, using TOML syntax: `framed = true`) in the front-matter,
2. type whatever you want in the body of a file,
3. restart the Hugo server,
4. you should see the box.

Remember that you can create these boxes inside every `_index` file.

The template for this is in: `layouts/_default/index.html:1-5`
