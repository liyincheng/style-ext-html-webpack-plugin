# style-ext-html-webpack-plugin for webpack 4
This plugin fixed problems for [style-ext-html-webpack-plugin](https://github.com/liyincheng/style-ext-html-webpack-plugin) whoes current version not supportes webpack 4. The funtionality is to extract CSS file in inline style.
```bash
npm i --save-dev style-ext-html-webpack-plugin-webpack-4
```
##Usage
```javascript
const HtmlWebpackPlugin = require('html-webpack-plugin');
const StyleExtHtmlWebpackPlugin = require('style-ext-html-webpack-plugin-webpack-4');

new HtmlWebpackPlugin({
    plugins: [
        new HtmlWebpackPlugin({
            filename: 'test.html',
            template: 'src/assets/test.html'
            // add script attributes here!
            attributes: {
                crossorigin: 'anonymous'
            }
        }),
        // this one should be placed after HtmlWebpackPlugin
        new StyleExtHtmlWebpackPlugin()
    ]
});
```


