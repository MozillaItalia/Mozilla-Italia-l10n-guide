# Documentation style guide

## General rules

These are some of the general rules to follow when writing and reviewing documentation for this repository:
* Address the reader as **you**, avoid using **we**.
* Avoid using generic terms.
* Avoid unnecessary empty lines in the document.

## Typography

* Lists: each list item should start with an uppercase letter, and end with a period (only exception when the item ends with a URL). Use the `*` markdown notation for each item.
* Use lowercase after colons, only one space after a period.
* Use proper quotes, like `“example”`, instead of straight double quotes.
* Use typographical apostrophes `’` instead of straight single quotes `'` (code fragments are the only exception).
* Use backticks `, bold, or italic to highlight text in a sentence, not quotes.
* Try to use links instead of putting URLs directly in the text. For example, `visit [this page](http://example.com)` should be preferred to `visit http://example.com`.
* Leave an empty line before and after code fragments, specify the language where possible. For example:

<pre>
This is some text.

```PHP
$test = 'test';
```

This is some other text.
</pre>

## Titles

* Use the dash syntax, leave one space after the dash, e.g. `# This is a title`.
* Use sentence case, avoid title case.
* Documents should always start with a 1st level title. There should be **only one** 1st level title across the document.
* Leave an empty line before and after each title. The only exception is the 1st level title at the beginning of the page.
* Make sure to follow a logic when using titles, e.g. a 3rd level title should be in a section starting with a 2nd level title of its own.

This is an example of a good structure:

```
# This is the main title for this document

## This is a section

This is some text.

### This is a subsection

This is some text.

## This is another section

This is some more text.
```

## Tools

[Atom](https://atom.io/) is the best tool for editing Markdown files:
* You can preview the content with `CTRL+SHIFT+M`. If you forget the shortcut, you can always use `CMD+SHIFT+P` to display the list of available commands, and search for `Markdown Preview: Toggle`.
* You can install a package called [smart-quotes-plus](https://atom.io/packages/smart-quotes-plus), which lets you swap straight quotes with curly ones. Once the package is installed, press `CTRL+ALT+'` to swap quotes on the entire document, or the text currently selected. Again, you can use `CMD+SHIFT+P` and search for `Smart Quote Plus: Smartreplace`. Only make sure to not swap `"` or `'` in code fragments where these characters are wanted.

To install packages in Atom, open the Preferences, select the *Install* panel on the left and search for the package you’re interested in.

[markdownlint](https://github.com/DavidAnson/markdownlint), a Markdown linter, is run on automation (Travis) for each pull request. If you want to use this tool on your system, make sure to install [Node.js](https://nodejs.org/en/), then run the following commands from the root of your repository (only once):

```BASH
$ git clone https://github.com/flodolo/l10ndocs-linter
$ npm --prefix ./l10ndocs-linter install ./l10ndocs-linter
```

At this point you can launch the linter with this command:

```BASH
$ node l10ndocs-linter/linter/markdownlint.js
Using config file: /your_path/documentation/l10ndocs-linter/linter/markdownlint.json
Searching path: /your_path/documentation

There are no linter errors.
```
