# Test: Watching single files in copy-webpack-plugin broken on Windows because of wrong path separator

Test for https://github.com/webpack-contrib/copy-webpack-plugin/issues/226

## Usage

Run this on Windows:

```
yarn install
yarn start
```

You will see in the log, that a file like `C:/xxx\test-copy-webpack-plugin-path-separator\copy.txt` was added to change tracking. Notice the forward slash after drive letter. When you change `copy.txt`, nothing happens.

When you try the same with `copy-webpack-plugin@v4.3.1` watching works fine.
