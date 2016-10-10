# David Majda’s ESLint configuration

This is ESLint configuration I use in my JavaScript projects. It assumes
development in ES2015+ compatible with Node.js 4.

## Philosophy

  1. **Generally be strict.** Don’t allow things that are most likely mistakes
     (e.g. `no-cond-assign`), don’t allow using mis-features (e.g.
     `no-sparse-arrays`), enforce best practices (e.g. `no-empty`).

  2. **Assume the author knows what he/she is doing.** Don’t disallow features
     just because they can be misused under certain circumstances (e.g.
     `no-eval`) or because some people find them confusing (e.g. `no-bitwise`).

  3. **Define unambiguous code style.** Most code style choices should be done
     mechanically and enforced by tooling.

  4. **Don’t check code quality issues.** This covers things like checking
     cyclomatic complexity or levels of nesting. Unlike code style, code quality
     is best assessed intelligently by humans.

## Installation

```console
$ npm install --save-dev eslint-config-dmajda
```

## Usage

Put the following into your `.eslintrc.json` file:

```json
{
  "extends": "dmajda"
}
```

## Development

I expect this configuration to evolve based on my experience and evolution of
ESLint. Any change which could lead to new errors being reported is considered
backwards incompatible and will cause incrementing of the major version.
