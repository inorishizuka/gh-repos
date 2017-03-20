
# gh-repos

 [![Support me on Patreon][badge_patreon]][patreon] [![Buy me a book][badge_amazon]][amazon] [![PayPal][badge_paypal_donate]][paypal-donations] [![Version](https://img.shields.io/npm/v/gh-repos.svg)](https://www.npmjs.com/package/gh-repos) [![Downloads](https://img.shields.io/npm/dt/gh-repos.svg)](https://www.npmjs.com/package/gh-repos)

> Get one or all the owner repositories from GitHub.

## :cloud: Installation

```sh
$ npm i --save gh-repos
```


## :clipboard: Example



```js
const githubRepos = require("gh-repos");

// Get a specific repository (the result will be an array containing one element)
githubRepos("IonicaBizau/git-stats", function (err, repos) {
    console.log(err || repos);
    // [ { id: 30538630,
    //     name: 'git-stats',
    //     full_name: 'IonicaBizau/git-stats',
    //     owner: { login: 'IonicaBizau', ...},
    //     private: false,
    //     ...
    //     subscribers_count: 52 } ]
});

// Get all my repositories
githubRepos("IonicaBizau", function (err, repos) {
    console.log(err || repos);
    // [ { id: 20149013,
    //     name: '3x3-equation-solver',
    //     full_name: 'IonicaBizau/3x3-equation-solver',
    //     owner: {...},
    //     ...
    //     default_branch: 'master' },
    //   { id: 48318047,
    //     name: 'add-subtract-date',
    //     full_name: 'IonicaBizau/add-subtract-date',
    //     owner: {...},
    //     ...
    //     default_branch: 'master' },
    //   ...
    //   { id: 21358670,
    //     name: 'youtube-topmost',
    //     full_name: 'IonicaBizau/youtube-topmost',
    //     owner: {...},
    //     ...
    //     default_branch: 'master' } ]
});

// Use a token
githubRepos("IonicaBizau", "your token", function (err, repos) {
    // ...
});
```

## :memo: Documentation


### `ghRepos(input, token, cb)`
Get one or all the owner repositories from GitHub.

#### Params
- **String** `input`: The GitHub owner or repository full name (`owner/repo`).
- **String** `token`: An optional GitHub token.
- **Function** `cb`: The callback function.



## :yum: How to contribute
Have an idea? Found a bug? See [how to contribute][contributing].


## :sparkling_heart: Support my projects

I open-source almost everything I can, and I try to reply everyone needing help using these projects. Obviously,
this takes time. You can integrate and use these projects in your applications *for free*! You can even change the source code and redistribute (even resell it).

However, if you get some profit from this or just want to encourage me to continue creating stuff, there are few ways you can do it:

 - Starring and sharing the projects you like :rocket:
 - [![PayPal][badge_paypal]][paypal-donations]—You can make one-time donations via PayPal. I'll probably buy a ~~coffee~~ tea. :tea:
 - [![Support me on Patreon][badge_patreon]][patreon]—Set up a recurring monthly donation and you will get interesting news about what I'm doing (things that I don't share with everyone).
 - **Bitcoin**—You can send me bitcoins at this address (or scanning the code below): `1P9BRsmazNQcuyTxEqveUsnf5CERdq35V6`

    ![](https://i.imgur.com/z6OQI95.png)

Thanks! :heart:


## :dizzy: Where is this library used?
If you are using this library in one of your projects, add it in this list. :sparkles:


 - [`gh-repeat`](https://github.com/IonicaBizau/gh-repeat#readme)—Repetitive actions on multiple GitHub repositories.

## :scroll: License

[MIT][license] © [Ionică Bizău][website]

[badge_patreon]: http://ionicabizau.github.io/badges/patreon.svg
[badge_amazon]: http://ionicabizau.github.io/badges/amazon.svg
[badge_paypal]: http://ionicabizau.github.io/badges/paypal.svg
[badge_paypal_donate]: http://ionicabizau.github.io/badges/paypal_donate.svg
[patreon]: https://www.patreon.com/ionicabizau
[amazon]: http://amzn.eu/hRo9sIZ
[paypal-donations]: https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=RVXDDLKKLQRJW
[donate-now]: http://i.imgur.com/6cMbHOC.png

[license]: http://showalicense.com/?fullname=Ionic%C4%83%20Biz%C4%83u%20%3Cbizauionica%40gmail.com%3E%20(https%3A%2F%2Fionicabizau.net)&year=2016#license-mit
[website]: https://ionicabizau.net
[contributing]: /CONTRIBUTING.md
[docs]: /DOCUMENTATION.md
