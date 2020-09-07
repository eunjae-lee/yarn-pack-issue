# README

Run

```
touch .env
yarn pack

The output contains `this-file-should-not-be-packed.js` and `.env`.
`.env` is included in `.gitignore`.

If you get rid of the line 8 from `package.json`

```
"!**/**tests**/**"
```

and try `yarn pack` again, then it doesn't contain them.

There seems to be an error regarding how yarn interprets `files` property when there is a negative expression.

I've confirmed this behaviour with yarn 1.16.0 and 1.22.5.
```

https://github.com/yarnpkg/yarn/issues/8332
