
# slush-ng

Use gulp & slush to act a bit like a more configurable brunch with minimal yeoman-like powers.

Basic project is a well structured & minimal AngularJS app that uses javascript & plain HTML & frameworks to ramp-up a project quickly.

It'd be a good idea to seperate the question/configurator into a module that can also be used by grunt/brunch/etc.

## build targets

### all skeletons

*  `build` - `['main-bower-files', 'concat']`
*  `serve` - `['watch', 'build', 'startServer', 'autoreload']`- `startServer` runs server/index.js, restarts if server-files change
*  `deploy` - `['build', 'minify', 'deployPush']` - `deployPush`

### deployPush

This is whatever is needed for the skeleton to send it's code to final production.  In the case of heroku or gh-pages, it will push it up, in the case of a mobile or nodewebkit app, it will build it.


## question flow

what kind of deployments will this app have?

*  I will work out deployment myself (uncheck others)
*  cordova
*  nodewebkit
*  gh-pages
*  heroku


what CSS framework do you want to use?

*  none
*  foundation (SASS-based)
*  bootstrap  (SASS/LESS-based)
*  ionic (SASS-based)


do you like LESS or SASS?

*  no - pre-build CSS for framework & add to CSS
*  LESS - if bootstrap, use source, else pre-build foundation/ionic SASS
*  SASS - if bootstrap, use bootstrap-SASS source, else use foundation/ionic source


do you need any of these?

*  ngRouter (uncheck angular-ui-router)
*  angular-ui-router (uncheck ngRouter)
*  ngCookie

## scaffolds

scaffolds should be aware of the above choices, when they generate things.