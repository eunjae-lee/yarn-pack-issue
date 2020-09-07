# README

If you run `yarn pack`, the output contains `this-file-should-not-be-packed.js`.

If you get rid of the line 8 from `package.json`

```
"!**/__tests__/**"
```

and try `yarn pack` again, then it doesn't contain it.

There seems to be an error regarding how yarn interprets `files` property when there is a negative expression.
