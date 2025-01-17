# solutions-of-errors

made for the amazing course available on awwwards: [Building an immersive creative website from scratch without frameworks by Luis Henrique Bizarro](https://www.awwwards.com/academy/course/building-an-immersive-creative-website-from-scratch-without-frameworks)

A repo of solutions related to huge bunch of errors
all thanks to community members.

Facing error downloading resources, then download from [this](https://github.com/LunacTec/floema_resources) repo provided by lunactec.
and also I made a repo which have commits according to the lecture of the course see [here](https://github.com/whizzbbig/webpack-boilerplate/commits/main)

# Tools i used while working with the course

- Favicon Generator [link](https://favicon.io/)
- Social Media Meta Tags Generator [link](https://metatags.io/)

# Note 
``` 
don't lose patience follow the course till the end of the slide and if you not able to counter
the error or bizzaro'ends showing no errors then come to this repo.
```

[Pull Request](https://github.com/whizzbbig/solutions-of-errors/pulls) to add more solutions of errors

## Errors 

- [You can use numbers for reference-style link definitions](#error-1)
- [Error: Invalid Configuration Object. Webpack has been initialised....](#error-2)
- [Error: 3](#error-3)
- [Error: 4](#error-4)
- [Error: [webpack-cli] Error: Unknown Option -p](#error-5)
- [Error: 6](#error-6)
- [Error: 7](#error-7)
- [Error: 8](#error-8)
- [Error: 9](#error-9)
- [Error: 10](#error-10)
- [Error: 11](#error-11)
- [Error: 12](#error-12)
- [Error: 13](#error-13)
- [Error: 14](#error-14)
- [Error: 15](#error-15)
- [Error: 16](#error-16)
- [Webpack taking time to compile :(](#error-17)
- [Failed to apply ESLint fixes to the document. Please consider opening an issue with steps to reproduce.](#error-18)
- [[nodemon] app crashed - waiting for file changes before starting...](#error-19)
- [bable-loader@8.2.2 requires a peer of @babel/core@^7.0.0 but none is installed. You must installed peer dependencies yourself](#error-20)
- [writeToDisk Error](#error-21)
- [cannot read property 'data' of undefined](#error-22)
- [ ERROR in unable to locate ](#error-23)
- [ TypeError: Prismic.getApi is not a function ](#error-24)
- [ Refused to apply style from 'http://localhost:8004/detail/main.css' because its MIME type ('text/html') is not a supported stylesheet MIME type, and strict MIME checking is enabled. ](#error-25)
- [ throw new TypeError('Only absolute URLs are supported') ](#error-26)
- [ Invalid options object. Image Minimizer Plugin has been initialized using an options object that does not match the API schema. ](#error-27)

## Questions
- [Question 1](#question-1)
- [Question 2](#question-2)
- [Question 3](#question-3)
- [Question 4](#question-4)
- [Question 5](#question-6)
- [Question 7](#question-7)
- [Question 8](#question-8)
- [Question 9](#question-9)
- [Question 10](#question-10)
- [Question 11](#question-11)


## Error 1
```
$ npm start
> floema@1.0.0 start
> npm run development
> floema@1.0.0 development
> webpack serve --progress --config webpack.config.development.js
[webpack-cli] Failed to load 'D:\Documents\dev\awwwards\floema\webpack.config.development.js' config
[webpack-cli] Error: Cannot find module './webpack-config'
Require stack:
- D:\Documents\dev\awwwards\floema\webpack.config.development.js
- D:\Documents\dev\awwwards\floema\node_modules\webpack-cli\lib\webpack-cli.js
- D:\Documents\dev\awwwards\floema\node_modules\webpack-cli\lib\bootstrap.js
- D:\Documents\dev\awwwards\floema\node_modules\webpack-cli\bin\cli.js
- D:\Documents\dev\awwwards\floema\node_modules\webpack\bin\webpack.js
    at Function.Module._resolveFilename (internal/modules/cjs/loader.js:880:15)
    at Function.Module._load (internal/modules/cjs/loader.js:725:27)
    at Module.require (internal/modules/cjs/loader.js:952:19)
    at require (D:\Documents\dev\awwwards\floema\node_modules\v8-compile-cache\v8-compile-cache.js:159:20)
    at Object.<anonymous> (D:\Documents\dev\awwwards\floema\webpack.config.development.js:4:16)
    at Module._compile (D:\Documents\dev\awwwards\floema\node_modules\v8-compile-cache\v8-compile-cache.js:192:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:1092:10)
    at Module.load (internal/modules/cjs/loader.js:928:32)
    at Function.Module._load (internal/modules/cjs/loader.js:769:14)
    at Module.require (internal/modules/cjs/loader.js:952:19) {
  code: 'MODULE_NOT_FOUND',
  requireStack: [
    'D:\\Documents\\dev\\awwwards\\floema\\webpack.config.development.js',
    'D:\\Documents\\dev\\awwwards\\floema\\node_modules\\webpack-cli\\lib\\webpack-cli.js',
    'D:\\Documents\\dev\\awwwards\\floema\\node_modules\\webpack-cli\\lib\\bootstrap.js',
    'D:\\Documets\\dev\\awwwards\\floema\\node_modules\\webpack-cli\\bin\\cli.js',
    'D:\\Documents\\dev\\awwwards\\floema\\node_modules\\webpack\\bin\\webpack.js'
  ]
}
 ``` 
 encountered by ``@walterlicinio#3771``

### Reason
```
could presist because of typo.
```

 ### Solution
``try to start again with the following lecture and follow the instructor carefully.``

## Error 2
![error:2](https://cdn.discordapp.com/attachments/838608259413835806/841670767628124200/unknown.png)
encounterd by ``@patmw#9134``

### Reason
``` 
This is because you're initialising the dev server in a way which is deprecated in webpack V5.
```

### Solution
```js
  devServer: {
    devMiddleware: {
      writeToDisk: true,
    },
  },
```

## Error 3

![error:3](https://user-images.githubusercontent.com/54703305/129493969-94f41c90-6a58-452c-9dfe-7e325c0ca426.png)
encountered by ``@Mitch D. Lincoln#8833 & @Alexelso#6992``

### Reason
```
The error is triggered by the missing of
``module.exports``
in webpack.config.js
```
### Solution
```
continue with the course later down the course after adding 
``const dirNode = 'node_modules' & module.exports`` 
to 
``webpack.config.js``
will fix the error ^
```

## Error 4
```
error saying '@babel/core is missing'
```

### Reason
```
Because it isn't installed in devDependencies and at bizzaro's end its installed globally
```

### Solution
``npm i -D @babel/core``
if not work try to install it globally by going to root directory

how to go to root directory:
```
in mac

user$-imac % cd ~
```
and run command like
``npm install @babel/core -g``

[Move To Errors List](#errors)

## Error 5

![image](https://user-images.githubusercontent.com/54703305/129494810-d8c17b75-8880-4e2e-aa4d-14e56c3747ec.png)

### Reason 
```
the -p flag is deprecated in the latest build of webpack v5
```

### Solution

use this in package.json

```json
  "scripts": {
    "start": "npm run development",
    "development": "webpack serve --progress --config webpack.config.development.js",
    "build": "webpack --progress --config webpack.config.build.js"
  },
  ```
  
  ## Error 6
![image](https://user-images.githubusercontent.com/54703305/129494894-3380f4a8-6603-4f78-9096-c8aa9553a1ae.png)

### Reason  
```
the problem is that you need to put the plugins outside the output object
```

### Solution
do this in webpack.config.build.js

```
const path = require("path");

const { merge } = require("webpack-merge");
const config = require("./webpack.config");

module.exports = merge(config, {
    mode: "production",

    plugins: [new CleanWebpackPlugin()],

    output: {
        path: path.join(__dirname, "public"),
    },
});
```

## Error 7
![image](https://user-images.githubusercontent.com/54703305/129495010-c3a5c4c2-f787-4f73-b056-486a6ac3a941.png)

### Reason
``
When you import something is like you are declaring a variable, that means you cannot import something, name it as a an then create a variable a.
``

### Solution 
name the import a diferent way

From:
```
import image from './image.png';

const image = 'Hello there, im a text';
```
To

```
import image from './image.png';

const text = 'Hello there, im a text';
```

[Move To Errors List](#errors)



## Error 8

![image](https://user-images.githubusercontent.com/54703305/129495056-ef17a530-7dc1-453b-8bfd-b6c86ba6eb1a.png)

### Reason & Solution
``
In order to work as expected, webpack need you to provide some conent inside the image folder! In this case, just put any image you want in the folder!
``

## Error 9
![image](https://user-images.githubusercontent.com/54703305/129495162-1971e68d-dc33-4705-9c11-55aae80727bf.png)

## Reason
``
Typo Issue 
``

## Solution

There can be typo issue in your prismic repo or you just miss somethings to add, to refactor it copy the json file given below and go to your [product](https://floaema.prismic.io/masks/product.json/) document JSON Editor just replace the old one with the one you copied right now. and you good to go !!

```json
{
  "Main" : {
    "uid" : {
      "type" : "UID",
      "config" : {
        "label" : "UID"
      }
    },
    "collection" : {
      "type" : "Link",
      "config" : {
        "select" : "document",
        "customtypes" : [ "collection" ],
        "label" : "Collection"
      }
    },
    "title" : {
      "type" : "Text",
      "config" : {
        "label" : "Title"
      }
    },
    "image" : {
      "type" : "Image",
      "config" : {
        "constraint" : { },
        "thumbnails" : [ ],
        "label" : "Image"
      }
    },
    "model" : {
      "type" : "Image",
      "config" : {
        "constraint" : { },
        "thumbnails" : [ ],
        "label" : "Model"
      }
    },
    "highlights" : {
      "type" : "Group",
      "config" : {
        "fields" : {
          "highlights_icon" : {
            "type" : "Select",
            "config" : {
              "options" : [ "Arrow", "Star" ],
              "default_value" : "Arrow",
              "label" : "Icon"
            }
          },
          "highlights_text" : {
            "type" : "Text",
            "config" : {
              "label" : "Text"
            }
          }
        },
        "label" : "Highlights"
      }
    },
    "informations" : {
      "type" : "Group",
      "config" : {
        "fields" : {
          "informations_label" : {
            "type" : "Text",
            "config" : {
              "label" : "Label"
            }
          },
          "informations_description" : {
            "type" : "Text",
            "config" : {
              "label" : "Description"
            }
          }
        },
        "label" : "Informations"
      }
    },
    "link_text" : {
      "type" : "Text",
      "config" : {
        "label" : "Shop it - Text"
      }
    },
    "link_url" : {
      "type" : "Link",
      "config" : {
        "label" : "Shop it - Link",
        "select" : null
      }
    }
  }
}
```


[Move To Errors List](#errors)


## Error 10

Getting this error when i try to run ``npm run development``

```sh
floema@1.0.0 start
npm run development


floema@1.0.0 development
webpack serve --progress --config webpack.config.development.js

D:\Awwwards-courses\Floema\app D:\Awwwards-courses\Floema\assets D:\Awwwards-courses\Floema\styles
[webpack-cli] Invalid configuration object. Webpack has been initialized using a configuration object that does not match the API schema.
 - configuration.output should be an object:
this is my webpack.config.development.js file:
```
![image](https://user-images.githubusercontent.com/54703305/129495214-5ab61f2b-8d2f-4f51-b3fe-c1da54012768.png)

### Reason

`` can be a typo issue. if not please do ask for it in our discord channel ``

### Solution
add this in your package.json file in "development"
```
"development": "webpack serve --progress --config webpack.config.development.js", 
```  

## Error 11

``I'm getting the following errors when I run npm start:``

![image](https://user-images.githubusercontent.com/54703305/129495263-19dbbe28-9f13-4518-8b1c-af52ce91291a.png)

### Reason
`` The Error Is because of the port using might be already in use. ``

### Solution 

``sudo kill PIDnumbergoeshere``
or
``pkill -f node``

#### For Windows

![Screenshot 2564-08-16 at 7 14 39 PM](https://user-images.githubusercontent.com/54703305/129573481-25701015-030f-4511-9ab3-534873d3bd54.png)


### Students Faced this error in some other possibilities
#### if you have ``exclude`` statements in your rules for babel 
``The do this``
![Screenshot 2564-08-16 at 7 22 23 PM](https://user-images.githubusercontent.com/54703305/129574611-3e045368-a76c-4e04-8b04-91666e1a8e82.png)


## Error 12
![image](https://user-images.githubusercontent.com/54703305/129574830-e51482bf-1f89-4283-a8be-567efa8cb462.png)

### Reason 
`` This is happening because you haven't installed concurrently globally.``

### Solution

``npm install -g concurrently`` by going to your root dir ``~``


[Move To Errors List](#errors)


## Error 13

```
Error: D:\Awwwards-courses\Floema\views\pages\home.pug:6:1

Unexpected block content


home.pug:
extends ../base.pug

block variables 
  - var template = 'home' 

block content 
  h1.collections__title Home


base.pug:

  body
    include ./partials/preloader
    include ./partials/navigation

    .content#content(data-template=template)
      block body
```

### Solution

Change ``block body`` to ``block content`` in base.pug

## Error 14
![image](https://user-images.githubusercontent.com/54703305/129580836-3c795929-a13c-4f51-878c-9b1957131a19.png)

### Answer 

[stackoverflow](https://stackoverflow.com/questions/34600932/npm-eperm-operation-not-permitted-on-windows)

## Error 15

``Hi I am at the implementation of pug prismic and express part. Sometimes the routing works perfectly fine, sometimes it throws this error. Especially when I navigate between /collections and /home, it has to fetch collection the second time , it will fail for sure.   Is it possible that Prismic is unstable for unpaid users? Thanks in advance.``
![image](https://user-images.githubusercontent.com/54703305/129581549-23249155-7b50-42c6-abce-9cd0fc92f878.png)

### Reason 
``bodyparser is commented``

### Solution
`` Use it``

but why to comment body parser. because a student acknowledged it as a depricated if you guys wants to use any other solution
then you can use this 

```app.use(express.json())
app.use(express.urlencoded())
```

[Move To Errors List](#errors)


## Error 16

![image](https://user-images.githubusercontent.com/54703305/129582106-20b2b6b2-6f42-4b4e-a2ec-24c237c9960b.png)

### Reason 

``It's an mini typo``

### Solution

``if section.slice_type == 'highlight'``
if this not able to solve the problem do follow the lecture again carefully ^

## Error 17

```
npm start

> floema@1.0.0 start /Users/desartist22/Desktop/Experience.me/floema
> concurrently --kill-others "npm run backend:development" "npm run frontend:development"

[0] 
[0] > floema@1.0.0 backend:development /Users/desartist22/Desktop/Experience.me/floema
[0] > nodemon app.js
[0] 
[1] 
[1] > floema@1.0.0 frontend:development /Users/desartist22/Desktop/Experience.me/floema
[1] > webpack serve --progress --config webpack.config.development.js
[1] 
[0] [nodemon] 2.0.12
[0] [nodemon] to restart at any time, enter `rs`
[0] [nodemon] watching path(s): *.*
[0] [nodemon] watching extensions: js,mjs,json
[0] [nodemon] starting `node app.js`
[0] Example app listening at http://localhost:3000
[1] <s> [webpack.Progress] 0% 
[1] 
[1] <s> [webpack.Progress] 1% setup initialize
[1] <s> [webpack.Progress] 1% setup initialize
[1] <s> [webpack.Progress] 3% setup watch run
[1] <s> [webpack.Progress] 3% setup watch run webpack-cli
[1] <s> [webpack.Progress] 3% setup watch run WebpackDevMiddleware
[1] <s> [webpack.Progress] 3% setup watch run
[1] <s> [webpack.Progress] 4% setup normal module factory
[1] <s> [webpack.Progress] 4% setup normal module factory
[1] <s> [webpack.Progress] 5% setup context module factory
[1] <s> [webpack.Progress] 5% setup context module factory
[1] <s> [webpack.Progress] 6% setup before compile
[1] <s> [webpack.Progress] 6% setup before compile ProgressPlugin
[1] <s> [webpack.Progress] 6% setup before compile
[1] <s> [webpack.Progress] 7% setup compile
[1] <s> [webpack.Progress] 7% setup compile ExternalsPlugin
[1] <s> [webpack.Progress] 7% setup compile webpack-dev-server
[1] <s> [webpack.Progress] 7% setup compile
[1] <s> [webpack.Progress] 8% setup compilation
[1] <s> [webpack.Progress] 8% setup compilation CopyPlugin
[1] <s> [webpack.Progress] 8% setup compilation mini-css-extract-plugin
[1] <s> [webpack.Progress] 8% setup compilation ArrayPushCallbackChunkFormatPlugin
[1] <s> [webpack.Progress] 8% setup compilation JsonpChunkLoadingPlugin
[1] <s> [webpack.Progress] 8% setup compilation StartupChunkDependenciesPlugin
[1] <s> [webpack.Progress] 8% setup compilation ImportScriptsChunkLoadingPlugin
[1] <s> [webpack.Progress] 8% setup compilation FetchCompileWasmPlugin
[1] <s> [webpack.Progress] 8% setup compilation FetchCompileAsyncWasmPlugin
[1] <s> [webpack.Progress] 8% setup compilation WorkerPlugin
[1] <s> [webpack.Progress] 8% setup compilation SplitChunksPlugin
[1] <s> [webpack.Progress] 8% setup compilation ResolverCachePlugin
[1] <s> [webpack.Progress] 8% setup compilation
[1] <s> [webpack.Progress] 9% setup compilation
[1] <s> [webpack.Progress] 9% setup compilation ProgressPlugin
[1] <s> [webpack.Progress] 9% setup compilation DefinePlugin
[1] <s> [webpack.Progress] 9% setup compilation mini-css-extract-plugin
[1] <s> [webpack.Progress] 9% setup compilation ImageMinimizerPlugin
[1] <s> [webpack.Progress] 9% setup compilation ImageMinimizerPlugin
[1] <s> [webpack.Progress] 9% setup compilation ChunkPrefetchPreloadPlugin
[1] <s> [webpack.Progress] 9% setup compilation ModuleInfoHeaderPlugin
[1] <s> [webpack.Progress] 9% setup compilation EvalDevToolModulePlugin
[1] <s> [webpack.Progress] 9% setup compilation JavascriptModulesPlugin
[1] <s> [webpack.Progress] 9% setup compilation JsonModulesPlugin
[1] <s> [webpack.Progress] 9% setup compilation AssetModulesPlugin
[1] <s> [webpack.Progress] 9% setup compilation EntryPlugin
[1] <s> [webpack.Progress] 9% setup compilation EntryPlugin
[1] <s> [webpack.Progress] 9% setup compilation RuntimePlugin
[1] <s> [webpack.Progress] 9% setup compilation InferAsyncModulesPlugin
[1] <s> [webpack.Progress] 9% setup compilation DataUriPlugin
[1] <s> [webpack.Progress] 9% setup compilation FileUriPlugin
[1] <s> [webpack.Progress] 9% setup compilation CompatibilityPlugin
[1] <s> [webpack.Progress] 9% setup compilation HarmonyModulesPlugin
[1] <s> [webpack.Progress] 9% setup compilation AMDPlugin
[1] <s> [webpack.Progress] 9% setup compilation RequireJsStuffPlugin
[1] <s> [webpack.Progress] 9% setup compilation CommonJsPlugin
[1] <s> [webpack.Progress] 9% setup compilation LoaderPlugin
[1] <s> [webpack.Progress] 9% setup compilation LoaderPlugin
[1] <s> [webpack.Progress] 9% setup compilation NodeStuffPlugin
[1] <s> [webpack.Progress] 9% setup compilation APIPlugin
[1] <s> [webpack.Progress] 9% setup compilation ExportsInfoApiPlugin
[1] <s> [webpack.Progress] 9% setup compilation WebpackIsIncludedPlugin
[1] <s> [webpack.Progress] 9% setup compilation ConstPlugin
[1] <s> [webpack.Progress] 9% setup compilation UseStrictPlugin
[1] <s> [webpack.Progress] 9% setup compilation RequireIncludePlugin
[1] <s> [webpack.Progress] 9% setup compilation RequireEnsurePlugin
[1] <s> [webpack.Progress] 9% setup compilation RequireContextPlugin
[1] <s> [webpack.Progress] 9% setup compilation ImportPlugin
[1] <s> [webpack.Progress] 9% setup compilation SystemPlugin
[1] <s> [webpack.Progress] 9% setup compilation ImportMetaPlugin
[1] <s> [webpack.Progress] 9% setup compilation URLPlugin
[1] <s> [webpack.Progress] 9% setup compilation DefaultStatsFactoryPlugin
[1] <s> [webpack.Progress] 9% setup compilation DefaultStatsPresetPlugin
[1] <s> [webpack.Progress] 9% setup compilation DefaultStatsPrinterPlugin
[1] <s> [webpack.Progress] 9% setup compilation JavascriptMetaInfoPlugin
[1] <s> [webpack.Progress] 9% setup compilation EnsureChunkConditionsPlugin
[1] <s> [webpack.Progress] 9% setup compilation RemoveEmptyChunksPlugin
[1] <s> [webpack.Progress] 9% setup compilation MergeDuplicateChunksPlugin
[1] <s> [webpack.Progress] 9% setup compilation SideEffectsFlagPlugin
[1] <s> [webpack.Progress] 9% setup compilation FlagDependencyExportsPlugin
[1] <s> [webpack.Progress] 9% setup compilation NamedModuleIdsPlugin
[1] <s> [webpack.Progress] 9% setup compilation NamedChunkIdsPlugin
[1] <s> [webpack.Progress] 9% setup compilation DefinePlugin
[1] <s> [webpack.Progress] 9% setup compilation TerserPlugin
[1] <s> [webpack.Progress] 9% setup compilation TemplatedPathPlugin
[1] <s> [webpack.Progress] 9% setup compilation RecordIdsPlugin
[1] <s> [webpack.Progress] 9% setup compilation WarnCaseSensitiveModulesPlugin
[1] <s> [webpack.Progress] 9% setup compilation EntryPlugin
[1] <s> [webpack.Progress] 9% setup compilation EntryPlugin
[1] <s> [webpack.Progress] 9% setup compilation EntryPlugin
[1] <s> [webpack.Progress] 9% setup compilation ProvidePlugin
[1] <s> [webpack.Progress] 9% setup compilation
[1] <s> [webpack.Progress] 10% building
[1] <s> [webpack.Progress] 10% building 0/1 entries 0/0 dependencies 0/0 modules
[1] ℹ ｢wds｣: Project is running at http://localhost:8080/
[1] ℹ ｢wds｣: webpack output is served from /
[1] ℹ ｢wds｣: Content not from webpack is served from /Users/desartist22/Desktop/Experience.me/floema
[1] <s> [webpack.Progress] 10% building import loader ./node_modules/babel-loader/lib/index.js
[1] <s> [webpack.Progress] 10% building 0/5 entries 3/5 dependencies 0/2 modules
[1] <s> [webpack.Progress] 10% building import loader ./node_modules/mini-css-extract-plugin/dist/loader.js
[1] <s> [webpack.Progress] 10% building import loader ./node_modules/css-loader/dist/cjs.js
[1] <s> [webpack.Progress] 10% building import loader ./node_modules/sass-loader/dist/cjs.js
[1] <s> [webpack.Progress] 10% building import loader ./node_modules/postcss-loader/dist/cjs.js
[1] <s> [webpack.Progress] 10% building 0/5 entries 5/5 dependencies 0/3 modules
[1] <s> [webpack.Progress] 10% building import loader ./node_modules/file-loader/dist/cjs.js
[1] <s> [webpack.Progress] 10% building import loader ./node_modules/image-minimizer-webpack-plugin/dist/loader.js
[1] <s> [webpack.Progress] 10% building 0/5 entries 23/29 dependencies 1/13 modules
[1] <s> [webpack.Progress] 10% building 0/5 entries 39/42 dependencies 5/22 modules
[1] You did not set any plugins, parser, or stringifier. Right now, PostCSS does nothing. Pick plugins for your case on https://www.postcss.parts/ and use them in postcss.config.js.
[1] <s> [webpack.Progress] 10% building 0/5 entries 51/54 dependencies 13/28 modules
[1] <s> [webpack.Progress] 21% building 1/5 entries 52/55 dependencies 20/29 modules
[1] <s> [webpack.Progress] 32% building 2/5 entries 52/55 dependencies 20/29 modules
[1] <s> [webpack.Progress] 42% building 3/5 entries 62/62 dependencies 32/34 modules
```

### Reason
``its taking that much time because of imageMinimizerPlugin``

### Solution 
``By disabling it in webpack.config.js file will solve the problem ^``

it happens sometimes because of not enought memory power or process power

[Move To Errors List](#errors)

## Error 18 
``Failed to apply ESLint fixes to the document. Please consider opening an issue with steps to reproduce.``
I've installed those plugins also and also did what bizarro did but then also nothing happens :'(

### Solution 1
``npm install eslint -g``
which will install eslint globally. install it in your root directory ^ `~`

if this not solve your problem then follow with the [Solution 2](###solution-2)

#### Check for the plugin in globally by passing this ``npm list -g`` command on terminal which will log out the plugins which are installed globally like this
![Screenshot 2564-08-17 at 12 19 41 AM](https://user-images.githubusercontent.com/54703305/129614601-26b222e8-8ead-479c-a4da-4ac5ad97d605.png)
so if you not find the plugin you installed for globally you can follow with solution 2

### Solution 2
if you use this ``./node_modules/.bin/eslint --init`` in your project will solve your problem ^. after this you don't need any ``.editorconfig``. file but if you have it then no worries there :)

## Error 19
``[nodemon] app crashed - waiting for file changes before starting...`` 

### Reason
``Usually happens when the servers process in the background.``

### Solution
``so you need to stop them form terminal``
#### For MacOs, Linux
``pkill -f node``
kill them all by running on terminal and it will work fine ^

#### For Windows
```
 1. Go to the task manager
 2. Then search-for node.js server-side javascript
 3. Then right click on it and end-task from the processes. 
 4. then do npm start and it will work fine ^
 ```
 
 ## Error 20
 ![image](https://user-images.githubusercontent.com/54703305/130318292-ddb7d3c6-32a3-4560-8485-85b0e9886d1c.png)
### Reason
there can be two reason that this error showing.
* @babel/core isn't installed globally in your os.
* @babel/core ins't in your devDependencies

### Solution

#### Solution 1
try installing @babel/core into your devDependencies by passing following command
```npm install @babel/core --save-dev```

``if Solution 1 didn't help then try following solution 2 ( will definetly work ^ )`` 
#### Solution 2
try installing @babel/core ``globally``. there wasn't any error at bizzaro side where he hasn't installed this plugin in devDependencies this is because the plugin was installed globally try passing this command into your root ``~`` directory. To go in root directory pass this command ``cd ~`` ``npm install @babel/core -g``

[Move To Errors List](#errors)


## Error 21

![Screenshot 2564-10-01 at 5 19 45 PM](https://user-images.githubusercontent.com/54703305/135615436-19c86d49-ed91-459d-b2ca-c8211d709130.png)

### Reason
Webpack change the way we write ``writeToDisk``

### Solution 
Try doing this 

```js
devServer: {
    devMiddleware: {
        writeToDisk: true,
    }
}
```

## Error 22 

![Cannot read property 'data' of undefined](https://media.discordapp.net/attachments/838608259413835806/842905509917229066/unknown.png)

### Solution 
```js
app.get('/about', (req, res) => {

      initApi(req).then(api => {
        api.query(
          Prismic.Predicates.any('document.type', ['meta', 'about']),
        ).then(response => {
          const{results} = response
          const[about, meta] = results
          console.log(about, meta)
          res.render('pages/about', {
            meta,
            about
          });
        });
      });
    });
 ```
 go to `/about` it'll work for sure and if you also want it to work on `pages/home` just for the sake to get rid of error.
 then, you can go with same steps just edit the `about` with `home` 
 
 for example:
 ```js
res.render('pages/about', {
    meta,
    about
});
```
to this

```js
res.render('pages/home', {
    meta,
    home
});
```

### If you still getting weird errors then try using this [repo](https://github.com/whizzbbig/floema) which exactly has the same progress you made till now 😁

## Error 23

```
 ERROR in unable to locate '/Users/sandra/Dev/UAS/shared/**/*' glob 
```

### Reason

You have to add some random file for a time just to make it to work and let you to complete making your boilerplate 

### Solution

taking this error as an example add some `.txt` file to make it work something like `shared/cool.txt`
still had some problems just give some time to the repo i provided above and try to find the solution

## Error 24
```
when I go to npm start in the terminal it's ok.
but, when I open the about page I receive the error "TypeError: Prismic.getApi is not a function". 
```

### Reason
Prismic updated their API to v6.

### Solution 1

follow the migration guide from v5 to v6 [here](https://github.com/whizzbbig/webpack-boilerplate/commits/main)

### Alternate Solution
Prismic recently got an update so by using the respective package that had been used in the project will resolve the issue if you
not want to migrate from v5 to v6 try this simple solution :).
`npm install @prismicio/client@5.1.0 --save`

## Error 25

```
Refused to apply style from 'http://localhost:8004/detail/main.css' because its MIME type ('text/html') is not a supported stylesheet MIME type, and strict MIME checking is enabled.
```

## Reason
It happens when you set an incorrect URL to the file or when your server isn't configured properly. In the result, the browser DOESN'T get the stylesheet

## Solution
so here in our case we can add following things to resolve the issue firstly you have to add `type=text/css` in link and also don't forget to add `/` before 
`main.css` file same goes with js file when we going to link it in future lecture you're gonna expereience this issue especially with route `/detail` if you not
add `/` before the `index.js` file

Example:
main.css
```pug
link(rel="stylesheet" type="text/css" href="/main.css")
```
index.js
```pug
script(src="/main.js")
```

## Error 26 
```
throw new TypeError('Only absolute URLs are supported');
```

## Reason 
You would have downloaded the repo i provided which has commits according to lectures but while trying to run it at localhost you have encountered this error it is because you haven't have .env file in your dir

## Solution
to fix this issue make the file named `.env` to the folder and paste these Prismic Credentials to resolve the error or you can add your own prismic credentials.

```sh
PRISMIC_ACCESS_TOKEN=MC5ZWDhQMVJFQUFDTUFHazRI.77-9aSLvv73vv73vv73vv73vv70h77-9dGhvYO-_ve-_vRFpD--_vXcd77-9f--_ve-_ve-_ve-_ve-_ve-_ve-_vXE
PRISMIC_CLIENT_ID=YX8P1REAACIAGk4G
PRISMIC_CLIENT_SECRET=7559e127bfd27950ed7ff6ed58331b80
PRISMIC_ENDPOINT=https://floema-ice.prismic.io/api/v2

GOOGLE_ANALYTICS=GOOGLE_ANALYTICS
```

## Error 27
```
Invalid options object. Image Minimizer Plugin has been initialized using an options object that does not match the API schema.
```

## Reason
Webpack updated their way of using image-minimizer-webpack-plugin in version @3.2.3

## Solution
```js
new ImageMinimizerPlugin({
  minimizer: {
    implementation: ImageMinimizerPlugin.imageminMinify,
     options: {
       plugins: [
       // interlaced: Interlace gif for progressive rendering.
       ['gifsicle', { interlaced: true }],

       // progressive: Lossless conversion to progressive.
       ['jpegtran', { progressive: true }],

       // optimizationLevel (0-7): The optimization level 0 enables a set of
       // optimization operations that require minimal effort. There will be
       // no changes to image attributes like bit depth or color type, and no
       // recompression of existing IDAT datastreams. The optimization level
       // 1 enables a single IDAT compression trial. The trial chosen is what
       // OptiPNG thinks it’s probably the most effective.
       ['optipng', { optimizationLevel: 7 }],
     ],
    },
  }
}),
```


[Move To Errors List](#errors)

# Questions


## Question 1
```js
why does the development config script need:

output: {
    path: path.resolve(__dirname, "public"),
  },
``` 
by @interactive-harp#6998

### Answer
``Here your telling webpack that the file it needs to send to the browser is this one!`` by @lunactec#1507

## Question 2
``why do we need to use express.js when we could use a webpack related plugin to use local server?`` by @interactive-harp#6998

### Answer
``For the ruting system and the integration of prismic
plus its really easy to transform this website into a funcitonal ecommerce just becuase of that
That means that, becuase of using express, every major change related to the product its easier to handle
This is a really good resource to learn node and express.js basics! -> https://youtu.be/Oe421EPjeBE`` by @lunactec#1507

## Question 3

``What if we don't need any back-end or e-commerce.... then no neeed for express`` by @interactive-harp#6998

### Answer

``If you implement the routing client-side then yes, i think so`` by @lunactec#1507
``If you don't want to have a CMS and BE integration, using routes is completely fine.`` by @bizarro#7465 ( course instructor )

## Question 4

``is there an advantage to use prismic than those?`` by @HenHeym#1915

### Answer 4

`` think possibly the Express integration. Usually it's just hard to do it in other CMS.`` by @bizarro#7645 ( course instructor )

`` Internationalization is one for sure
https://payloadcms.com/#express -> This one is in my scope! They have an integration with express too `` by @lunactec@1507

## Question 5

``if you ever need to implement a store in one of your sites, do you start from the same base you have, or do you use something else? For example on garoaskincare, how did you do it?`` by @HenHeym#1915

### Answer 5 

``y``

## Question 6

``does digital ocean and express need eachothers support? to put our site on digital ocean, do we need express/ a backend?
usually i use github pages thats why wondering`` by @interactive-harp#6998

### Answer 6 

``Digital ocean its a cloud provider that let us deploy our code in there. In it self, it has built in support for express, yes. You can also reffer the last 2 classes to get more information about the deployment process. It depends of the implementation, but you dont really need a backend to deploy in a cloud provider!`` by @lunactec#1507

## Question 7

``to use connect with a cms, a backend such as express is needed right?`` by @interactive-harp#6998

### Answer 7

``Not really, it depends on the cms your using
You can implement prismic without backend
https://prismic.io/docs/technologies/integrating-with-an-existing-project-javascript`` by @lunactec#1507

## Question 8 

``Whats the downfall of client over backend implementation?`` by @interactive-harp#6998

### Answer 8
``Well, i dont think there is an special reason implementing a backend instead of a full client aprouch in this specific project, rather than bizarro's personal preference and experience
Personally, i really like the backend aproach, it makes it simpler to maintain and i like backend routing too! Plus you can easely integrate alot of services! And its maybe more productive than a full client aproach.`` by @lunactec#1507

``don't let the back end implementation let you down. I know it's not 100% related, but someone will ask you to make an editable website in the future, and you'll know how to do it. :smile:
After you do the full course, if you check out this repo here: https://github.com/lhbizarro/bizar.ro/. You'll be able to understand how to do everything in GH Pages.`` by @bizarro#7645

## Question 9
``is  prismic allows a client to edit the site without them needing to know code?`` by @sweatythonk#7907

### Answer 9
``Yeah, if they have access to the primsic project, you can do that!`` by @lunactec#1507


## Question 10

``What about the connection issue? I doubt this is a Prismic issue, because for me it works half of the time. but It's frustrating to restart the server and wait for it to work.`` by @Weijie#0237

### Answer 10
``First put the express parsers, maybe that solve part of the issue!`` by @lunactec#1507

## Question 11
``is there any repo from where I can check and compare the commit with my code and see where I messed up with the code?`` by @anonymous

### Answer 11
Yes, you can able to see commits if you download the source code zip from the site and open it in Github Desktop and check its history to see the commits.

here is another repo made by me which has commits according to lectures of course 😁 
```
https://github.com/whizzbbig/floema_/commits/main
```
by @whizzbbig#3445
