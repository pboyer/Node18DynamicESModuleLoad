# Description

This project demonstrates how to load an ES Module in node.js 18 using the `--require` command line flag by using a dynamic `import` call.

# Run

```
npm run app
```

# Behavior

-- `app.js` is the node module to be run. It can be an ES module or Common JS module.
-- `shim.cjs` is a commonjs module that loads `esmodule.js`
--- `esmodule.js` loads `esmodule2.js` using an `import` statement

As `shim.cjs` uses a dynamic import, `app.js` is run _before_ the imported code in `esmodule.js` and `esmodule2.js`.
