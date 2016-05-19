# dc-tabs

## dc-tabs is no longer maintained. Please consider using [ivy-tabs](https://github.com/IvyApp/ivy-tabs) instead.

**NOTE**: This addon is a port from [http://instructure.github.io/ic-tabs](http://instructure.github.io/ic-tabs) into an ember-cli addon. The port was made out of samheucks fork on the master branch @ad25734fdb and then changed to lazy render tabs. This fork was made as ic-tabs seemed to have stopped being maintained and it needed updating to the latest ember version and tools.

Todos:
- Port tests to ember-cli
- Tie together examples page
- Travis CI
- Demo page


<!---
[![Build Status](https://travis-ci.org/instructure/dc-tabs.png?branch=master)](https://travis-ci.org/instructure/dc-tabs)
--->

[WAI-ARIA][wai-aria] accessible tab component for [Ember.js][ember].

<!---
Demo
----

http://instructure.github.io/dc-tabs
--->

Installation
------------

```sh
$ ember install:addon dc-tabs

```

Usage
-----

```handlebars
{{#dc-tabs}}
  {{#dc-tab-list}}
    {{#dc-tab}}Foo{{/dc-tab}}
    {{#dc-tab}}Bar{{/dc-tab}}
    {{#dc-tab}}Baz{{/dc-tab}}
  {{/dc-tab-list}}

  {{#dc-tab-panel}}
    <h2>Foo</h2>
  {{/dc-tab-panel}}

  {{#dc-tab-panel}}
    <h2>Bar</h2>
  {{/dc-tab-panel}}

  {{#dc-tab-panel}}
    <h2>Baz</h2>
  {{/dc-tab-panel}}
{{/dc-tabs}}
```

- associations between tabs and tab-panes are inferred by order.
- `dc-tab-list` must be an immediate child of `dc-tabs`
- `dc-tab` must be an immediate child of `dc-tab-list`
- `dc-tab-panel` must be an immediate child of `dc-tabs`

Styles can be imported as 'dc-tabs' into your app style sheet.

Options
-------

- `{{dc-tabs selected-index=prop}}` - binds the active-index to prop,
  mostly useful for `queryParams`.

Contributing
------------

```sh
$ git clone <this repo>
$ ember install
$ ember server / ember test
```
