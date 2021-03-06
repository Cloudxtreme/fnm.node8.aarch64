
# git-package-json

 [![Patreon](https://img.shields.io/badge/Support%20me%20on-Patreon-%23e6461a.svg)][patreon] [![PayPal](https://img.shields.io/badge/%24-paypal-f39c12.svg)][paypal-donations] [![AMA](https://img.shields.io/badge/ask%20me-anything-1abc9c.svg)](https://github.com/IonicaBizau/ama) [![Version](https://img.shields.io/npm/v/git-package-json.svg)](https://www.npmjs.com/package/git-package-json) [![Downloads](https://img.shields.io/npm/dt/git-package-json.svg)](https://www.npmjs.com/package/git-package-json) [![Get help on Codementor](https://cdn.codementor.io/badges/get_help_github.svg)](https://www.codementor.io/johnnyb?utm_source=github&utm_medium=button&utm_term=johnnyb&utm_campaign=github)

> Get the package.json contents from git repositories.

## :cloud: Installation

```sh
$ npm i --save git-package-json
```


## :clipboard: Example



```js
const gitPackageJson = require("git-package-json");

gitPackageJson("git@github.com:IonicaBizau/git-stats.git", function (err, data) {
    console.log(err || data);
    // { name: 'git-stats',
    //   version: '2.9.2',
    //   description: 'Local git statistics including GitHub-like contributions calendars.',
    //   main: 'lib/index.js',
    //   ...
    //   _id: 'git-stats@2.9.2' }
});

// Takes the repo from GitHub
gitPackageJson("nuvipannu/ascii-heart", function (err, data) {
    console.log(err || data);
    // { name: 'ascii-heart',
    //   version: '2.0.0',
    //   description: 'Create ASCII hearts using Node.js.',
    //   main: 'lib/index.js',
    //   ...
    //   _id: 'ascii-heart@2.0.0' }
});
```

## :memo: Documentation


### `gitPackageJson(input, sha, callback)`
Gets the `package.json` file contents by passing the git url.

#### Params
- **String|GitSource** `input`: A [`GitSource`](https://github.com/IonicaBizau/git-source) object or the git url.
- **String** `sha`: An optional sha-ish (branch, version, commit sha etc) to set the project state.
- **Function** `callback`: The callback function.



## :yum: How to contribute
Have an idea? Found a bug? See [how to contribute][contributing].


## :moneybag: Donations

Another way to support the development of my open-source modules is
to [set up a recurring donation, via Patreon][patreon]. :rocket:

[PayPal donations][paypal-donations] are appreciated too! Each dollar helps.

Thanks! :heart:

## :dizzy: Where is this library used?
If you are using this library in one of your projects, add it in this list. :sparkles:


 - [`package.json`](https://github.com/IonicaBizau/pkg.json#readme)—Get the package.json content either from npm or from a git repository.
 - [`pkg.json`](https://github.com/IonicaBizau/pkg.json#readme)—Get the package.json content either from npm or from a git repository.

## :scroll: License

[MIT][license] © [Ionică Bizău][website]

[patreon]: https://www.patreon.com/ionicabizau
[paypal-donations]: https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=RVXDDLKKLQRJW
[donate-now]: http://i.imgur.com/6cMbHOC.png

[license]: http://showalicense.com/?fullname=Ionic%C4%83%20Biz%C4%83u%20%3Cbizauionica%40gmail.com%3E%20(http%3A%2F%2Fionicabizau.net)&year=2016#license-mit
[website]: http://ionicabizau.net
[contributing]: /CONTRIBUTING.md
[docs]: /DOCUMENTATION.md
