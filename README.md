example#testFunction1 `npm test` will output

```
    /home/nam/projects/jest-babel-lodash-issue/src/example.js:3
    var testFunction1 = /* istanbul ignore next */exports.testFunction1 = ();
                                                                           ^
    
    SyntaxError: Unexpected token )
```

example#testFunction2 `npm test` will output

```
    ReferenceError: /home/nam/projects/jest-babel-lodash-issue/src/example.js: Container is falsy
      
      at NodePath._replaceWith (node_modules/babel-traverse/lib/path/replacement.js:170:11)
```

Removing `collectCoverage` from `package.json` lets the tests run without failure.
