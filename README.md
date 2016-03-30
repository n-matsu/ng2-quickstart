# Angular 2 QuickStart Source

This repository holds the TypeScript source code of the [angular.io quickstart](https://angular.io/docs/ts/latest/quickstart.html),
the foundation for most of the documentation samples and potentially a good starting point for your application.

## Create a new project based on the QuickStart

Clone this repo into new project folder (e.g., `my-proj`).
```bash
$ git clone  https://github.com/angular/quickstart  my-proj
$ cd my-proj
```

We have no intention of updating the source on `angular/quickstart`.
Discard everything "git-like" by deleting the `.git` folder.
```bash
$ rm -rf .git
```

### Create a new git repo
You could [start writing code](#start-development) now and throw it all away when you're done.
If you'd rather preserve your work under source control, consider taking the following steps.

Initialize this project as a *local git repo* and make the first commit:
```bash
$ git init
$ git add .
$ git commit -m "Initial commit"
```

Create a *remote repository* for this project on the service of your choice.

Grab its address (e.g. *`https://github.com/<my-org>/my-proj.git`*) and push the *local repo* to the *remote*.
```bash
$ git remote add origin <repo-address>
$ git push -u origin master
```
### Start development

Install the npm packages described in the `package.json` and verify that it works:

```bash
$ npm install
$ npm start
```
You're ready to write your application.

Remember the npm scripts in `package.json`:

* `npm start` - runs the compiler and a server at the same time, both in "watch mode".
* `npm run tsc` - runs the TypeScript compiler once.
* `npm run tsc:w` - runs the TypeScript compiler in watch mode; the process keeps running, awaiting changes to TypeScript files and re-compiling when it sees them.
* `npm run lite` - runs the [lite-server](https://www.npmjs.com/package/lite-server), a light-weight, static file server, written and maintained by
[John Papa](https://github.com/johnpapa) and
[Christopher Martin](https://github.com/cgmartin)
with excellent support for Angular apps that use routing.
* `npm run typings` - runs the typings tool.
* `npm run postinstall` - called by *npm* automatically *after* it successfully completes package installation. This script installs the TypeScript definition files this app requires.



```bash
55411 verbose stack Error: angular2-quickstart@1.0.0 postinstall: `typings install`
55411 verbose stack Exit status 1
55411 verbose stack     at EventEmitter.<anonymous> (/home/vagrant/.nvm/versions/node/v5.9.1/lib/node_modules/npm/lib/utils/lifecycle.js:239:16)
55411 verbose stack     at emitTwo (events.js:100:13)
55411 verbose stack     at EventEmitter.emit (events.js:185:7)
55411 verbose stack     at ChildProcess.<anonymous> (/home/vagrant/.nvm/versions/node/v5.9.1/lib/node_modules/npm/lib/utils/spawn.js:24:14)
55411 verbose stack     at emitTwo (events.js:100:13)
55411 verbose stack     at ChildProcess.emit (events.js:185:7)
55411 verbose stack     at maybeClose (internal/child_process.js:850:16)
55411 verbose stack     at Process.ChildProcess._handle.onexit (internal/child_process.js:215:5)
55412 verbose pkgid angular2-quickstart@1.0.0
55413 verbose cwd /tmp/test
55414 error Linux 2.6.32-573.el6.x86_64
55415 error argv "/home/vagrant/.nvm/versions/node/v5.9.1/bin/node" "/home/vagrant/.nvm/versions/node/v5.9.1/bin/npm" "install"
55416 error node v5.9.1
55417 error npm  v3.7.3
55418 error code ELIFECYCLE
55419 error angular2-quickstart@1.0.0 postinstall: `typings install`
55419 error Exit status 1
55420 error Failed at the angular2-quickstart@1.0.0 postinstall script 'typings install'.
55420 error Make sure you have the latest version of node.js and npm installed.
55420 error If you do, this is most likely a problem with the angular2-quickstart package,
55420 error not with npm itself.
55420 error Tell the author that this fails on your system:
55420 error     typings install
55420 error You can get information on how to open an issue for this project with:
55420 error     npm bugs angular2-quickstart
55420 error Or if that isn't available, you can get their info via:
55420 error     npm owner ls angular2-quickstart
55420 error There is likely additional logging output above.
55421 verbose exit [ 1, true ]```
