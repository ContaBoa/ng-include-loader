# ng-include-loader

angular ng-include loader for webpack

If you use webpack and angular ng-include directive, you may need this loader

The loader will look for the `ng-include` directive in the current template and load the corresponding partial file.

## Install:
```
npm install -D angular-include-loader
```

### Usage examples:

Using the module context to resolve the partial file path:
```
{test: /\.html$/, use: ['raw-loader', 'ng-include-loader']}
```

Manually defining a base path:
```
{
  test: /\.html$/,
  use: [
    'html-loader',
    {
      loader: 'ng-include-loader',
      options: {
        basePath: path.resolve(__dirname, "src"),
      }
    }
  ]
}
```
