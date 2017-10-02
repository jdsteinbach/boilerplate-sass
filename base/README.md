# Base

`/base/` is the **simple foundation** of your project that all other CSS builds on.  It supposes very little.

## Contents

It mostly consists of `reset.css` from [Eric Meyer](http://meyerweb.com/eric/tools/css/reset/).

### `_helpers.scss`

`helpers` is a small collection of utility classes that can be added to HTML elements **that do not already have a class** if you need that element to do something in particular, like `float: right`.

But if the element already has a class, just add the rule to that class ruleset instead of using `@extend` or adding an additional class from `helpers` to the HTML element.

### `_functions.scss`

This partial imports the partials in `/base/functions/`. New functions should be added to their own partials and imported / documented in this file.

### `_mixins.scss`

This partial imports the partials in `/base/mixins/`. New mixins should be added to their own partials and imported / documented in this file.

### `_extends.scss`

This partial imports the partials in `/base/extends/`. New extends should be added to their own partials and imported / documented in this file.

_Note on `@extend`_ - try not to use this. If you do, expect to be pushed for a solid justification during your PR review.

### `_variables.scss`

This partial imports the partials in `/base/variables/`. New variables should be added to the appropriate existing partial and new variable collections should be added to new partials, then imported / documented in this file.

## Additions

If you have a function, mixin, or variable set that's valuable enough to to include in all the themes, [submit a PR](https://github.com/jdsteinbach/base/pulls).