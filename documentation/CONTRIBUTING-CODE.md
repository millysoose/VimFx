# Contributing code

Feel free to contribute stuff that you think might help people, but please
remember that VimFx is a dead project so there’s a risk that your pull request
won’t be merged.

See [README.md] for more information.

[README.md]: ../README.md


## Localizations

Contribute your localization! Copy the `extension/locale/en-US` directory and go
wild! Usually, it’s best to stick to the master branch.

Tip: If you’re translating into, for example, Swedish, run `gulp sync-locales
--sv-SE?` to see how many percent is done. All lines (including line numbers)
that don’t differ compared to “en-US” are also printed, letting you know what’s
left to do. Substitute “sv-SE” with the locale you’re working on.

Also, don’t worry if you can’t get a 100% difference compared to “en-US.”
Sometimes text strings are very short and will look identical in both languages.
That’s completely OK.


## Code

Create a new topic branch, based on either master or develop.

    git checkout -b my-topic-branch master
    # or
    git checkout -b my-topic-branch develop

Code! Try to follow these simple rules:

- Always use parentheses when calling functions.
- Always use braces for object literals.
- Always use explicit `return`s, unless the function is a one-liner.
- Always use single quotes, unless you use interpolation.
- Prefer interpolation over concatenation, both for strings and regexes.
- Always use the following forms (not any aliases):
  - `true` and `false`
  - `==` and `!=`
  - `and` and `or`
  - `not`
- Never use `++` and `--`.
- Never put spaces directly inside `[]` and `{}`.
- Never put spaces before or more than one space after `:` in object literals.
- Never use `when ... then` in `switch`es; replace `then` with a newline.
- Avoid vertical alignment of code (such as aligning `=`s).
- Comment when necessary. Comments should be full sentences.
- Keep lines at most 80 characters long.
- Indent using two spaces.
- Commit no `console.log(...)`s (but do use them when debugging).

See [tools.md] for how to **build,** **lint,** and **run the tests.**

Break up your pull request in several commits if necessary. The first line of
commit messages should be a short summary. If needed, add a blank line and then
a nicely formatted markdown description.

Finally send a pull request to same branch as you based your topic branch on
(master or develop).

[tools.md]: tools.md
