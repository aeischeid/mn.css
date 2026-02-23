# Contributing to mn.css

mn.css becomes better for everyone when people like you help make it better!

Before contributing, please read the [code of conduct](CODE_OF_CONDUCT.md). Also, you agree that your contributions will be licensed under this project's [MIT License](../LICENSE.md).

## Overview

Please take a moment to read through the following guidelines:

- [Get started](#get-started)
- [Find issues to work on](#find-issues-to-work-on)
- [Add or change styles](#add-or-change-styles)
- [Create your pull request](#create-your-pull-request)
- [Project structure](#project-structure)

<br>

> **Quickstart**:
> 1. clone the repo - open files!
> 2. view the index.html in a browser
> 3. make sure your changes look good in the 3 major browser engines (firefox/Gecko, Safari/Webkit, Chome/Blink)
> 4. lint / format changes using Biome. `bunx --bun @biomejs/biome format --write`

<br>

## Get started

1. Get a copy of the repository. It is recommended to [fork](https://github.com/aeisched/mn.css/fork) it first and clone to your machine using `git`.

2. Open the files in your favorite editor. 

3. Open index.html in your browser. (no dev server provided for now)

> Alternatively, you can develop in Repl.it, a supercool in-browser IDE! Just click this button: [![Run on Repl.it](https://repl.it/badge/github/aeischeid/mn.css)](https://repl.it/github/aeischeid/mn.css)

## Find issues to work on

If you are new to contributing open-source software, you can start by picking any relevant issue that is [tagged with **`good first issue`**](
https://github.com/aeischeid/mn.css/contribute).

Also, everyone is welcome to contribute on issues [tagged with **`help wanted`**, you can find it filtered here](https://github.com/aeischeid/mn.css/issues?q=is%3Aopen+is%3Aissue+label%3A%22help+wanted%22).

## Add or change styles

There are a few rules for working in the mn.css source code:

1. The styles should not use any IDs. and where possible prefer style rules that only target HTML elements or attributes, .

2. Specify shared colors directly the theme files

  ❌ Bad:
  ```css
  color: #fff;
  ```

  ✔ Good:
  ```css
  color: var(--text-bright);
  ```

3. Reuse existing colors where possible. Before introducing a new color to our palette, check if one of the existing colors fits your needs.

4. If you introduce a new color variable, make sure to test it both in dark light modes 

## Create your pull request

Once you're happy with your changes, you need to **commit** them, create a **changelog** and **submit a pull request**.

A few general rules of thumb about what makes a good pull request:

- Make sure that your pull request covers a small and well defined scope
- Make small commits with clear and explainful messages
- Provide a clear description about your contribution on GitHub

### Commit

When you commit code, some checks should run to make sure that it match the project's coding style – a process called [**Linting**](https://www.freecodecamp.org/news/what-is-linting-and-how-can-it-save-you-time). It will also verify that all **colors are accessible**, which means they need to have enough contrast to be easily readable.

<details>
  <summary>ℹ A note about puppeteer and WSL</summary>
  <br>
  <blockquote>
    The accessibility checks use puppeteer, a tool that uses Chrome to render websites "headlessly", without a visible interface. In some environments like the <a href="https://aka.ms/wsl">Windows Subsystem for Linux</a>, you'll need to manually configure and run an X-Server in order for puppeteer to work.
  </blockquote>
</details>

<br>

### Submit a Pull Request

Once your changes have been committed and you've created a changelog, you'll want to submit a pull request

Be sure to provide a clear description of what your pull request includes. If your pull request will close an existing issue, make sure to write `Closes #[id]` in the pull request description, where `[id]` is replaced by the issue your pull request will close.

After submitting a pull request, it will need to be reviewed by a maintainer of the project before being merged. You may be asked to make some changes to your pull request.

After your change has been reviewed and merged, you can celebrate as the newest contributor to the project! 🎉

## Project structure

TODO:
