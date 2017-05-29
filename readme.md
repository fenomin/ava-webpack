# ava-webpack

> Crude webpack enabled runner for AVA

## Installation

```
npm install ava-webpack --save-dev
```

## Usage example (almost as crude as the implementation - sorry)

*webpack.config-test.js* (using [ts-loader](https://github.com/TypeStrong/ts-loader))

```
'use strict';

module.exports = {
    resolve: {
        extensions: ['.ts', '.tsx', '.js'],
        alias: {}
    },
    module: {
        loaders: [
            {
                test: /\.tsx?$/,
                loader: 'ts-loader'
            }
        ]
    }
};

```

*package.json*

```
{
	"devDependencies": {
		"@types/enzyme": "^2.4.30",
		"ava": "^0.19.1",
		"ava-webpack": "^1.0.6",
		"ts-loader": "2.0.3",
		"enzyme": "^2.4.1",
		"rimraf": "^2.5.3",
		"typescript": "2.3.2",
		"webpack": "2.4.1"
	},
	"scripts": {
		"ava-test": "ava-webpack --webpack-config ./webpack.config-test.js"
	},
    "ava": "^0.19.1"
}

```
