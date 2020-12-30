# Markdown Loader
A markdown loader for webpack using markdown-it.

## installation

```bash
npm install --save-dev webpack-markdown-loader
```

## usage

```
const path = require('path')
const HtmlWebpackPlugin = require('html-webpack-plugin')


module.exports = {
	entry: {
		index: './src/js/index.js'
	},

	module: {
		rules: [
			{
				test: /\.md$/,
				use: [
				{
					loader: 'html-loader'
				},
				{
					loader: 'webpack-markdown-loader',
					options: {}
				}],
			},
		]
	},

	plugins: [
		new HtmlWebpackPlugin({
      filename: 'index.html',
      template: './src/views/index.html',
		})
```