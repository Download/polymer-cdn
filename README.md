# polymer-cdn <sup><sub>v2.0.1</sub></sup>
**A mirror of Polymer's components so that they can be used directly from CDN**

![Polymer CDN is powered by MaxCDN](http://i.imgur.com/9obTXpk.png)

```
❗  Polymer CDN now supports Polymer 2! Please [report](https://github.com/download/polymer-cdn/issues) any issues you may find.
```

## How to use
In general, given an element named `my-cool-element`, the CDN url for it will be:
```
https://cdn.rawgit.com/download/polymer-cdn/2.0.1/lib/my-cool-element/my-cool-element.html
```
To be sure, browse this repo and copy-paste the url to the raw version into [RawGit](https://rawgit.com).

## Try a pen
Try hacking on this [Codepen](http://codepen.io/StijnDeWitt/pen/EyPyyL).

## Versioning
As this repo groups a whole set of components, versioning is tricky. For now I've decided to
follow the Polymer version number and add an extra number behind it for updates that did not
involve a change of the Polymer version. It's important to remember that this repo does not
(can not) follow semantic versioning guidelines and that it's version numbers indicate not
much more than which versions came before which and after which other versions.

Make sure you always link to a specific version and not to `master`, as that would mean your
code could change right under your nose. Something you don't want in production! Also, for
this same reason, I recommend forking this repo and including from your own fork, so you'll
have full control over it.

To see available versions and select one, use the `Branch` dropdown menu and select one of
the `tags`. You can then browse that version of the Repo. Browse to the file you want to include
and copy the url to it's `raw` version. Throw that into [RawGit](https://rawgit.com) and you'll
have a url to a file on CDN that never expires from cache and is not throttled or limited
in bandwidth in any way.

![Branch selection in GitHub](https://camo.githubusercontent.com/8dbe1c395f07374e7d435880cc6804513989fea4/687474703a2f2f692e696d6775722e636f6d2f447867774872362e706e67)

## Missing something?
This repository aims to be a complete set of the standard Polymer components, grouped in such
a way that (transitive) dependencies can be correctly resolved for all components. If you are
missing some (version of) a component, please [create an issue](https://github.com/Download/polymer-cdn/issues)
explaining what should be changed and I'll do my best to implement it.

In the meanwhile, you can *fork this project* and apply the needed updates to your
own fork. It's a pretty simple process. Have a look at the [Contribution Guide](https://github.com/Download/polymer-cdn/blob/master/CONTRIBUTING.md)
which explains it in more detail.


## Contents
All the libraries available in polymer-cdn can be found side-by-side in the [lib](https://github.com/Download/polymer-cdn/tree/2.0.1/lib) subfolder.

Some of the libraries depend on other libraries. We call those other libraries the dependencies of the library.
These dependencies will also be pulled into your page when you include such a library.
If the dependencies themselves depend on yet other libraries, these dependencies of dependencies will also be
pulled into your page, et cetera until the full dependency tree has been loaded. We call this transitive
dependency resolution and it's built in to the way Web Components work.

The bower output below lists, for each library included in this CDN, the dependencies of that library.
These dependencies are themselves also listed at the top-level, so you can work out the entire dependency
tree for a library by carefully examining this diagram.

```sh
polymer-cdn#2.0.1
├─┬ app-elements#1.0.0
│ ├─┬ app-layout#1.0.1 (latest is 2.0.0)
│ │ ├─┬ iron-flex-layout#1.3.7 (latest is 2.0.0)
│ │ │ └── polymer#1.9.2 (latest is 2.0.1)
│ │ ├─┬ iron-media-query#1.0.8 (latest is 2.0.0)
│ │ │ └─┬ polymer#1.9.2 (latest is 2.0.1)
│ │ │   └── webcomponentsjs#1.0.1 incompatible with ^0.7.24 (0.7.24 available, latest is 1.0.1)
│ │ ├─┬ iron-resizable-behavior#1.0.6 (latest is 2.0.1)
│ │ │ └── polymer#1.9.2
│ │ ├── iron-scroll-target-behavior#1.1.1 (latest is 2.0.0)
│ │ └── polymer#1.9.2 (latest is 2.0.1)
│ ├─┬ app-localize-behavior#1.0.2 (latest is 2.0.0)
│ │ ├── intl-messageformat#1.3.0
│ │ ├─┬ iron-ajax#1.4.4 (latest is 2.0.2)
│ │ │ ├── polymer#1.9.2 (latest is 2.0.1)
│ │ │ └─┬ promise-polyfill#1.0.1 (latest is 2.0.0)
│ │ │   └─┬ polymer#1.9.2
│ │ │     └── webcomponentsjs#1.0.1
│ │ └── polymer#1.9.2 (latest is 2.0.1)
│ ├─┬ app-pouchdb#1.0.0 (latest is 2.1.1)
│ │ ├─┬ app-storage#2.0.2 incompatible with ~1.0.0 (1.0.1 available, latest is 2.0.2)
│ │ │ └── polymer#1.9.2 (2.0.1 available)
│ │ ├── polymer#1.9.2 (latest is 2.0.1)
│ │ ├── pouchdb#6.2.0
│ │ ├── pouchdb-find#0.10.5
│ │ └─┬ promise-polyfill#1.0.1
│ │   └─┬ polymer#1.9.2
│ │     └── webcomponentsjs#1.0.1
│ ├─┬ app-route#1.0.1 (latest is 2.0.0)
│ │ ├── iron-location#0.8.11 (latest is 2.0.1)
│ │ └── polymer#1.9.2 (latest is 2.0.1)
│ └── app-storage#2.0.2 incompatible with ^1.0.0 (1.0.1 available, latest is 2.0.2)
├── firebase-sdk extraneous
├─┬ gold-elements#1.0.1
│ ├─┬ gold-cc-cvc-input#1.0.10
│ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-form-element-behavior#1.0.7 (latest is 2.0.0)
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ ├─┬ iron-icon#1.0.13 (latest is 2.0.0)
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-meta#1.1.3 (latest is 2.0.0)
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └── polymer#1.9.2
│ │ ├── paper-input#1.1.24 (latest is 2.0.1)
│ │ ├─┬ paper-styles#1.3.1 (latest is 2.0.0)
│ │ │ ├── font-roboto#1.0.2
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ └── polymer#1.9.2
│ ├─┬ gold-cc-expiration-input#1.1.3
│ │ ├── iron-a11y-keys-behavior#1.1.9 (latest is 2.0.0)
│ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-form-element-behavior#1.0.7
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ ├─┬ iron-validatable-behavior#1.1.2 (latest is 2.0.0)
│ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ ├─┬ iron-validator-behavior#1.0.2 (latest is 2.0.0)
│ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ ├── paper-input#1.1.24
│ │ ├─┬ paper-styles#1.3.1
│ │ │ ├── font-roboto#1.0.2
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ └── polymer#1.9.2
│ ├─┬ gold-cc-input#1.0.7
│ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-form-element-behavior#1.0.7
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ ├─┬ iron-icon#1.0.13
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-validator-behavior#1.0.2
│ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ ├── paper-input#1.1.24
│ │ ├─┬ paper-styles#1.3.1
│ │ │ ├── font-roboto#1.0.2
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ └─┬ polymer#1.9.2
│ │   └── webcomponentsjs#1.0.1
│ ├─┬ gold-email-input#1.0.9
│ │ ├─┬ iron-form-element-behavior#1.0.7
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ ├─┬ iron-icon#1.0.13
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └── polymer#1.9.2
│ │ ├── paper-input#1.1.24
│ │ ├─┬ paper-styles#1.3.1
│ │ │ ├── font-roboto#1.0.2
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ └── polymer#1.9.2
│ ├─┬ gold-phone-input#1.1.0
│ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-form-element-behavior#1.0.7
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ ├─┬ iron-input#1.0.11 (latest is 2.0.0)
│ │ │ ├─┬ iron-a11y-announcer#1.0.6 (latest is 2.0.0)
│ │ │ │ └── polymer#1.9.2 (latest is 2.0.1)
│ │ │ ├─┬ iron-validatable-behavior#1.1.2
│ │ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ ├── paper-input#1.1.24
│ │ ├─┬ paper-styles#1.3.1
│ │ │ ├── font-roboto#1.0.2
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ └── polymer#1.9.2 (latest is 2.0.1)
│ └─┬ gold-zip-input#1.0.6
│   ├─┬ iron-form-element-behavior#1.0.7
│   │ └─┬ polymer#1.9.2
│   │   └── webcomponentsjs#1.0.1
│   ├─┬ iron-icon#1.0.13
│   │ ├─┬ iron-flex-layout#1.3.7
│   │ │ └── polymer#1.9.2
│   │ ├─┬ iron-meta#1.1.3
│   │ │ └─┬ polymer#1.9.2
│   │ │   └── webcomponentsjs#1.0.1
│   │ └── polymer#1.9.2
│   ├─┬ iron-validator-behavior#1.0.2
│   │ ├─┬ iron-meta#1.1.3
│   │ │ └─┬ polymer#1.9.2
│   │ │   └── webcomponentsjs#1.0.1
│   │ └─┬ polymer#1.9.2
│   │   └── webcomponentsjs#1.0.1
│   ├── paper-input#1.1.24
│   ├─┬ paper-styles#1.3.1
│   │ ├── font-roboto#1.0.2
│   │ ├─┬ iron-flex-layout#1.3.7
│   │ │ └── polymer#1.9.2
│   │ └─┬ polymer#1.9.2
│   │   └── webcomponentsjs#1.0.1
│   └── polymer#1.9.2
├─┬ google-web-components#1.1.1
│ ├─┬ firebase-element#1.0.16
│ │ ├── firebase#4.1.2 incompatible with ^2.3.1 (2.4.2 available, latest is 4.1.2)
│ │ └─┬ polymer#1.9.2
│ │   └── webcomponentsjs#1.0.1
│ ├─┬ google-analytics#1.2.3
│ │ ├── ga-api-utils#0.2.0 (latest is 0.7.0)
│ │ ├─┬ google-chart#1.1.2
│ │ │ ├─┬ google-apis#1.1.7
│ │ │ │ ├─┬ iron-jsonp-library#1.0.5
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ ├─┬ iron-ajax#1.4.4
│ │ │ │ ├── polymer#1.9.2
│ │ │ │ └─┬ promise-polyfill#1.0.1
│ │ │ │   └─┬ polymer#1.9.2
│ │ │ │     └── webcomponentsjs#1.0.1
│ │ │ ├─┬ polymer#1.9.2
│ │ │ │ └── webcomponentsjs#1.0.1
│ │ │ └─┬ promise-polyfill#1.0.1
│ │ │   └─┬ polymer#1.9.2
│ │ │     └── webcomponentsjs#1.0.1
│ │ ├─┬ google-signin#1.3.7
│ │ │ ├── font-roboto#1.0.2
│ │ │ ├─┬ google-apis#1.1.7
│ │ │ │ ├─┬ iron-jsonp-library#1.0.5
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ ├── iron-flex-layout#1.3.7
│ │ │ ├─┬ iron-icon#1.0.13
│ │ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-iconset-svg#1.1.1
│ │ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ ├─┬ paper-material#1.0.7
│ │ │ │ ├─┬ paper-styles#1.3.1
│ │ │ │ │ ├── font-roboto#1.0.2
│ │ │ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ │ │ └── polymer#1.9.2
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ paper-ripple#1.0.10
│ │ │ │ ├── iron-a11y-keys-behavior#1.1.9
│ │ │ │ └── polymer#1.9.2
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ ├─┬ polymer#1.9.2
│ │ │ └── webcomponentsjs#1.0.1
│ │ └─┬ promise-polyfill#1.0.1
│ │   └─┬ polymer#1.9.2
│ │     └── webcomponentsjs#1.0.1
│ ├─┬ google-apis#1.1.7
│ │ ├─┬ iron-jsonp-library#1.0.5 (latest is 2.0.0)
│ │ │ └── polymer#1.9.2
│ │ └─┬ polymer#1.9.2
│ │   └── webcomponentsjs#1.0.1
│ ├─┬ google-calendar#1.0.3
│ │ ├── google-apis#1.1.7
│ │ ├── google-signin#1.3.7
│ │ └─┬ polymer#1.9.2
│ │   └── webcomponentsjs#1.0.1
│ ├─┬ google-castable-video#1.0.3
│ │ └─┬ polymer#1.9.2
│ │   └── webcomponentsjs#1.0.1
│ ├─┬ google-chart#1.1.2
│ │ ├─┬ google-apis#1.1.7
│ │ │ ├─┬ iron-jsonp-library#1.0.5
│ │ │ │ └── polymer#1.9.2
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ ├─┬ iron-ajax#1.4.4
│ │ │ ├── polymer#1.9.2
│ │ │ └─┬ promise-polyfill#1.0.1
│ │ │   └─┬ polymer#1.9.2
│ │ │     └── webcomponentsjs#1.0.1
│ │ ├─┬ polymer#1.9.2
│ │ │ └── webcomponentsjs#1.0.1
│ │ └─┬ promise-polyfill#1.0.1
│ │   └─┬ polymer#1.9.2
│ │     └── webcomponentsjs#1.0.1
│ ├─┬ google-feeds#1.0.2
│ │ ├── google-apis#1.1.7
│ │ ├─┬ iron-jsonp-library#1.0.5
│ │ │ └── polymer#1.9.2
│ │ └─┬ polymer#1.9.2
│ │   └── webcomponentsjs#1.0.1
│ ├─┬ google-hangout-button#1.0.2
│ │ ├─┬ google-apis#1.1.7
│ │ │ ├─┬ iron-jsonp-library#1.0.5
│ │ │ │ └── polymer#1.9.2
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ └── polymer#1.9.2
│ │ └─┬ polymer#1.9.2
│ │   └── webcomponentsjs#1.0.1
│ ├─┬ google-map#1.2.0
│ │ ├── google-apis#1.1.7
│ │ ├── iron-resizable-behavior#1.0.6 (latest is 2.0.1)
│ │ ├── iron-selector#1.5.3 (latest is 2.0.0)
│ │ └── polymer#1.9.2 (latest is 2.0.1)
│ ├─┬ google-sheets#1.0.6
│ │ ├── google-apis#1.1.7
│ │ ├── google-signin#1.3.7
│ │ ├─┬ iron-ajax#1.4.4
│ │ │ ├── polymer#1.9.2
│ │ │ └─┬ promise-polyfill#1.0.1
│ │ │   └─┬ polymer#1.9.2
│ │ │     └── webcomponentsjs#1.0.1
│ │ └── polymer#1.9.2 (latest is 2.0.1)
│ ├─┬ google-signin#1.3.7
│ │ ├── font-roboto#1.0.2
│ │ ├─┬ google-apis#1.1.7
│ │ │ ├─┬ iron-jsonp-library#1.0.5
│ │ │ │ └── polymer#1.9.2
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ ├── iron-flex-layout#1.3.7 (latest is 2.0.0)
│ │ ├─┬ iron-icon#1.0.13
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-iconset-svg#1.1.1 (latest is 2.0.0)
│ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ ├─┬ paper-material#1.0.7 (latest is 2.0.0)
│ │ │ ├─┬ paper-styles#1.3.1
│ │ │ │ ├── font-roboto#1.0.2
│ │ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └── polymer#1.9.2
│ │ ├─┬ paper-ripple#1.0.10 (latest is 2.0.0)
│ │ │ ├── iron-a11y-keys-behavior#1.1.9 (latest is 2.0.0)
│ │ │ └── polymer#1.9.2
│ │ └─┬ polymer#1.9.2
│ │   └── webcomponentsjs#1.0.1
│ ├─┬ google-streetview-pano#1.0.4
│ │ ├── google-apis#1.1.7
│ │ ├── iron-resizable-behavior#1.0.6 (latest is 2.0.1)
│ │ └── polymer#1.9.2 (latest is 2.0.1)
│ ├─┬ google-url-shortener#1.0.2
│ │ ├─┬ google-apis#1.1.7
│ │ │ ├─┬ iron-jsonp-library#1.0.5
│ │ │ │ └── polymer#1.9.2
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ └─┬ polymer#1.9.2
│ │   └── webcomponentsjs#1.0.1
│ ├─┬ google-youtube#1.3.0
│ │ ├─┬ google-apis#1.1.7
│ │ │ ├─┬ iron-jsonp-library#1.0.5
│ │ │ │ └── polymer#1.9.2
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ ├─┬ iron-localstorage#1.0.6 (latest is 2.0.0)
│ │ │ └── polymer#1.9.2
│ │ └─┬ polymer#1.9.2
│ │   └── webcomponentsjs#1.0.1
│ ├─┬ google-youtube-upload#1.1.2 (latest is 2.0.0)
│ │ ├── cors-upload-sample#37c97848a2
│ │ ├─┬ google-signin#1.3.7
│ │ │ ├── font-roboto#1.0.2
│ │ │ ├─┬ google-apis#1.1.7
│ │ │ │ ├─┬ iron-jsonp-library#1.0.5
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ ├── iron-flex-layout#1.3.7
│ │ │ ├─┬ iron-icon#1.0.13
│ │ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-iconset-svg#1.1.1
│ │ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ ├─┬ paper-material#1.0.7
│ │ │ │ ├─┬ paper-styles#1.3.1
│ │ │ │ │ ├── font-roboto#1.0.2
│ │ │ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ │ │ └── polymer#1.9.2
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ paper-ripple#1.0.10
│ │ │ │ ├── iron-a11y-keys-behavior#1.1.9
│ │ │ │ └── polymer#1.9.2
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ └─┬ polymer#1.9.2
│ │   └── webcomponentsjs#1.0.1
│ └─┬ polymerfire#0.9.7 (latest is 2.1.0)
│   ├── app-storage#2.0.2 incompatible with ^0.9.0 (0.9.8 available, latest is 2.0.2)
│   ├── firebase#4.1.2 incompatible with ^3.0 (3.9.0 available, latest is 4.1.2)
│   └── polymer#1.9.2 (latest is 2.0.1)
├─┬ iron-elements#1.0.10
│ ├─┬ iron-a11y-announcer#1.0.6
│ │ └── polymer#1.9.2
│ ├─┬ iron-a11y-keys#1.0.9 (latest is 2.0.0)
│ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ └── polymer#1.9.2
│ │ └── polymer#1.9.2
│ ├─┬ iron-a11y-keys-behavior#1.1.9 (latest is 2.0.0)
│ │ └── polymer#1.9.2
│ ├─┬ iron-ajax#1.4.4
│ │ ├── polymer#1.9.2
│ │ └─┬ promise-polyfill#1.0.1
│ │   └─┬ polymer#1.9.2
│ │     └── webcomponentsjs#1.0.1
│ ├─┬ iron-autogrow-textarea#1.0.15 (latest is 2.0.0)
│ │ ├─┬ iron-behaviors#1.0.18
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ │ └── polymer#1.9.2
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-form-element-behavior#1.0.7
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ ├─┬ iron-validatable-behavior#1.1.2
│ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ └── polymer#1.9.2
│ ├─┬ iron-behaviors#1.0.18 (latest is 2.0.0)
│ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ └── polymer#1.9.2
│ │ └── polymer#1.9.2
│ ├─┬ iron-checked-element-behavior#1.0.6 (latest is 2.0.0)
│ │ ├─┬ iron-form-element-behavior#1.0.7
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ ├─┬ iron-validatable-behavior#1.1.2
│ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ └── polymer#1.9.2
│ ├─┬ iron-collapse#1.3.0 (latest is 2.0.0)
│ │ ├─┬ iron-resizable-behavior#1.0.6
│ │ │ └── polymer#1.9.2
│ │ └── polymer#1.9.2
│ ├─┬ iron-component-page#1.1.9 (latest is 3.0.0-rc.4)
│ │ ├── hydrolysis#1.24.1 (latest is 2.1.0)
│ │ ├─┬ iron-ajax#1.4.4
│ │ │ ├── polymer#1.9.2
│ │ │ └─┬ promise-polyfill#1.0.1
│ │ │   └─┬ polymer#1.9.2
│ │ │     └── webcomponentsjs#1.0.1
│ │ ├─┬ iron-doc-viewer#1.1.0 (latest is 3.0.0-rc.4)
│ │ │ ├─┬ marked-element#1.4.2 (latest is 2.1.1)
│ │ │ │ ├── marked#0.3.6
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ paper-button#1.0.15 (latest is 2.0.0)
│ │ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ ├─┬ paper-behaviors#1.0.13 (latest is 2.0.0)
│ │ │ │ │ ├─┬ iron-behaviors#1.0.18
│ │ │ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ │ │ │ │ └── polymer#1.9.2
│ │ │ │ │ │ └── polymer#1.9.2
│ │ │ │ │ ├─┬ iron-checked-element-behavior#1.0.6
│ │ │ │ │ │ ├─┬ iron-form-element-behavior#1.0.7
│ │ │ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ │ │ ├─┬ iron-validatable-behavior#1.1.2
│ │ │ │ │ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ │ │ └── polymer#1.9.2
│ │ │ │ │ ├─┬ paper-ripple#1.0.10
│ │ │ │ │ │ ├── iron-a11y-keys-behavior#1.1.9
│ │ │ │ │ │ └── polymer#1.9.2
│ │ │ │ │ └── polymer#1.9.2 (latest is 2.0.1)
│ │ │ │ ├─┬ paper-material#1.0.7
│ │ │ │ │ ├─┬ paper-styles#1.3.1
│ │ │ │ │ │ ├── font-roboto#1.0.2
│ │ │ │ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ │ │ │ └── polymer#1.9.2
│ │ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ paper-styles#1.3.1
│ │ │ │ ├── font-roboto#1.0.2
│ │ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ ├── polymer#1.9.2
│ │ │ └─┬ prism-element#1.2.0 (latest is 2.0.0)
│ │ │   ├── polymer#1.9.2
│ │ │   └── prism#1.6.0
│ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-icons#1.2.1
│ │ │ ├─┬ iron-icon#1.0.13
│ │ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-iconset-svg#1.1.1
│ │ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ ├─┬ iron-selector#1.5.3
│ │ │ └── polymer#1.9.2
│ │ ├─┬ paper-header-panel#1.1.7 (latest is 2.0.0)
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ └── polymer#1.9.2
│ │ ├─┬ paper-styles#1.3.1
│ │ │ ├── font-roboto#1.0.2
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ ├─┬ paper-toolbar#1.1.7 (latest is 2.0.0)
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ ├── paper-styles#1.3.1 (latest is 2.0.0)
│ │ │ └── polymer#1.9.2
│ │ └── polymer#1.9.2
│ ├─┬ iron-demo-helpers#1.2.6 (latest is 2.0.0)
│ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-icons#1.2.1
│ │ │ ├─┬ iron-icon#1.0.13
│ │ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-iconset-svg#1.1.1
│ │ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ ├─┬ iron-location#0.8.11
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ ├─┬ marked-element#1.4.2
│ │ │ ├── marked#0.3.6
│ │ │ └── polymer#1.9.2
│ │ ├─┬ paper-icon-button#1.1.6 (latest is 2.0.0)
│ │ │ ├─┬ iron-icon#1.0.13
│ │ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ paper-behaviors#1.0.13
│ │ │ │ ├─┬ iron-behaviors#1.0.18
│ │ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ │ │ │ └── polymer#1.9.2
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ ├─┬ iron-checked-element-behavior#1.0.6
│ │ │ │ │ ├─┬ iron-form-element-behavior#1.0.7
│ │ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ │ ├─┬ iron-validatable-behavior#1.1.2
│ │ │ │ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ ├─┬ paper-ripple#1.0.10
│ │ │ │ │ ├── iron-a11y-keys-behavior#1.1.9
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ paper-styles#1.3.1
│ │ │ │ ├── font-roboto#1.0.2
│ │ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └── polymer#1.9.2
│ │ ├─┬ paper-styles#1.3.1
│ │ │ ├── font-roboto#1.0.2
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ ├── polymer#1.9.2
│ │ └── prism-element#1.2.0 (latest is 2.0.0)
│ ├── iron-doc-viewer#1.1.0 (latest is 3.0.0-rc.4)
│ ├─┬ iron-dropdown#1.5.6 (latest is 2.0.0)
│ │ ├─┬ iron-behaviors#1.0.18
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ │ └── polymer#1.9.2
│ │ │ └── polymer#1.9.2
│ │ ├── iron-overlay-behavior#1.10.4 (latest is 2.0.0)
│ │ ├─┬ iron-resizable-behavior#1.0.6
│ │ │ └── polymer#1.9.2
│ │ ├─┬ neon-animation#1.2.5 (latest is 2.0.1)
│ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ ├─┬ iron-resizable-behavior#1.0.6
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-selector#1.5.3
│ │ │ │ └── polymer#1.9.2
│ │ │ ├── polymer#1.9.2
│ │ │ └── web-animations-js#2.2.5
│ │ └── polymer#1.9.2
│ ├─┬ iron-fit-behavior#1.2.6 (latest is 2.0.0)
│ │ └── polymer#1.9.2
│ ├─┬ iron-flex-layout#1.3.7
│ │ └── polymer#1.9.2
│ ├─┬ iron-form#1.1.5
│ │ ├─┬ iron-ajax#1.4.4
│ │ │ ├── polymer#1.9.2
│ │ │ └─┬ promise-polyfill#1.0.1
│ │ │   └─┬ polymer#1.9.2
│ │ │     └── webcomponentsjs#1.0.1
│ │ └── polymer#1.9.2
│ ├─┬ iron-form-element-behavior#1.0.7
│ │ └─┬ polymer#1.9.2
│ │   └── webcomponentsjs#1.0.1
│ ├─┬ iron-icon#1.0.13
│ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-meta#1.1.3
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ └── polymer#1.9.2
│ ├─┬ iron-icons#1.2.1 (latest is 2.0.1)
│ │ ├─┬ iron-icon#1.0.13
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-iconset-svg#1.1.1
│ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ └─┬ polymer#1.9.2
│ │   └── webcomponentsjs#1.0.1
│ ├─┬ iron-iconset#1.0.6 (latest is 2.0.0)
│ │ ├─┬ iron-meta#1.1.3
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ └─┬ polymer#1.9.2
│ │   └── webcomponentsjs#1.0.1
│ ├─┬ iron-iconset-svg#1.1.1
│ │ ├─┬ iron-meta#1.1.3
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ └─┬ polymer#1.9.2
│ │   └── webcomponentsjs#1.0.1
│ ├── iron-image#1.2.6 (latest is 2.1.1)
│ ├─┬ iron-input#1.0.11
│ │ ├─┬ iron-a11y-announcer#1.0.6
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-validatable-behavior#1.1.2
│ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ └─┬ polymer#1.9.2
│ │   └── webcomponentsjs#1.0.1
│ ├─┬ iron-jsonp-library#1.0.5
│ │ └── polymer#1.9.2
│ ├─┬ iron-label#1.0.2 (latest is 2.0.0)
│ │ └─┬ polymer#1.9.2
│ │   └── webcomponentsjs#1.0.1
│ ├─┬ iron-list#1.4.6 (latest is 2.0.1)
│ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-resizable-behavior#1.0.6
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-scroll-target-behavior#1.1.1 (latest is 2.0.0)
│ │ │ └── polymer#1.9.2
│ │ └── polymer#1.9.2
│ ├─┬ iron-localstorage#1.0.6
│ │ └── polymer#1.9.2
│ ├─┬ iron-location#0.8.11 (latest is 2.0.1)
│ │ └─┬ polymer#1.9.2
│ │   └── webcomponentsjs#1.0.1
│ ├─┬ iron-media-query#1.0.8
│ │ └─┬ polymer#1.9.2
│ │   └── webcomponentsjs#1.0.1
│ ├─┬ iron-menu-behavior#1.3.1 (latest is 2.0.0)
│ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-selector#1.5.3
│ │ │ └── polymer#1.9.2
│ │ └── polymer#1.9.2 (latest is 2.0.1)
│ ├─┬ iron-meta#1.1.3
│ │ └─┬ polymer#1.9.2
│ │   └── webcomponentsjs#1.0.1
│ ├─┬ iron-overlay-behavior#1.10.4 (latest is 2.0.0)
│ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-fit-behavior#1.2.6
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-resizable-behavior#1.0.6
│ │ │ └── polymer#1.9.2
│ │ └── polymer#1.9.2
│ ├─┬ iron-pages#1.0.9 (latest is 2.0.0)
│ │ ├─┬ iron-resizable-behavior#1.0.6
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-selector#1.5.3
│ │ │ └── polymer#1.9.2
│ │ └── polymer#1.9.2
│ ├─┬ iron-range-behavior#1.0.7 (latest is 2.0.0)
│ │ └── polymer#1.9.2
│ ├─┬ iron-resizable-behavior#1.0.6
│ │ └── polymer#1.9.2
│ ├── iron-scroll-target-behavior#1.1.1
│ ├─┬ iron-scroll-threshold#1.0.3 (latest is 2.0.0)
│ │ ├── iron-scroll-target-behavior#1.1.1
│ │ └── polymer#1.9.2
│ ├─┬ iron-selector#1.5.3 (latest is 2.0.0)
│ │ └── polymer#1.9.2
│ ├─┬ iron-signals#1.0.3
│ │ └─┬ polymer#1.9.2
│ │   └── webcomponentsjs#1.0.1
│ ├─┬ iron-swipeable-container#1.0.3
│ │ └── polymer#1.9.2
│ ├─┬ iron-test-helpers#1.4.1 (latest is 2.0.0)
│ │ └─┬ polymer#1.9.2
│ │   └── webcomponentsjs#1.0.1
│ ├─┬ iron-validatable-behavior#1.1.2
│ │ ├─┬ iron-meta#1.1.3
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ └─┬ polymer#1.9.2
│ │   └── webcomponentsjs#1.0.1
│ └─┬ iron-validator-behavior#1.0.2
│   ├─┬ iron-meta#1.1.3
│   │ └─┬ polymer#1.9.2
│   │   └── webcomponentsjs#1.0.1
│   └─┬ polymer#1.9.2
│     └── webcomponentsjs#1.0.1
├─┬ iron-page-url#0.7.3 extraneous (latest is 2.0.1)
│ └─┬ polymer#1.9.2
│   └── webcomponentsjs#1.0.1
├─┬ molecules#1.0.0
│ └─┬ marked-element#1.4.2
│   ├── marked#0.3.6
│   └── polymer#1.9.2
├─┬ neon-elements#1.0.0
│ └─┬ neon-animation#1.2.5
│   ├─┬ iron-meta#1.1.3
│   │ └─┬ polymer#1.9.2
│   │   └── webcomponentsjs#1.0.1
│   ├─┬ iron-resizable-behavior#1.0.6
│   │ └── polymer#1.9.2
│   ├─┬ iron-selector#1.5.3
│   │ └── polymer#1.9.2
│   ├── polymer#1.9.2
│   └── web-animations-js#2.2.5
├─┬ paper-elements#1.0.7
│ ├─┬ paper-badge#1.1.4 (latest is 2.0.0)
│ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-icon#1.0.13
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-resizable-behavior#1.0.6
│ │ │ └── polymer#1.9.2
│ │ ├─┬ paper-styles#1.3.1
│ │ │ ├── font-roboto#1.0.2
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ └── polymer#1.9.2
│ ├─┬ paper-behaviors#1.0.13
│ │ ├─┬ iron-behaviors#1.0.18
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ │ └── polymer#1.9.2
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-checked-element-behavior#1.0.6
│ │ │ ├─┬ iron-form-element-behavior#1.0.7
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ ├─┬ iron-validatable-behavior#1.1.2
│ │ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └── polymer#1.9.2
│ │ ├─┬ paper-ripple#1.0.10
│ │ │ ├── iron-a11y-keys-behavior#1.1.9
│ │ │ └── polymer#1.9.2
│ │ └── polymer#1.9.2
│ ├─┬ paper-button#1.0.15
│ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ └── polymer#1.9.2
│ │ ├─┬ paper-behaviors#1.0.13
│ │ │ ├─┬ iron-behaviors#1.0.18
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-checked-element-behavior#1.0.6
│ │ │ │ ├─┬ iron-form-element-behavior#1.0.7
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ ├─┬ iron-validatable-behavior#1.1.2
│ │ │ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ paper-ripple#1.0.10
│ │ │ │ ├── iron-a11y-keys-behavior#1.1.9
│ │ │ │ └── polymer#1.9.2
│ │ │ └── polymer#1.9.2
│ │ ├─┬ paper-material#1.0.7
│ │ │ ├─┬ paper-styles#1.3.1
│ │ │ │ ├── font-roboto#1.0.2
│ │ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └── polymer#1.9.2
│ │ └── polymer#1.9.2
│ ├─┬ paper-card#1.1.6 (latest is 2.0.0)
│ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-image#1.2.6 (latest is 2.1.1)
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ └── polymer#1.9.2
│ │ ├─┬ paper-material#1.0.7
│ │ │ ├─┬ paper-styles#1.3.1
│ │ │ │ ├── font-roboto#1.0.2
│ │ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └── polymer#1.9.2
│ │ ├── paper-styles#1.3.1
│ │ └── polymer#1.9.2
│ ├─┬ paper-checkbox#1.4.2 (latest is 2.0.0)
│ │ ├─┬ iron-checked-element-behavior#1.0.6
│ │ │ ├─┬ iron-form-element-behavior#1.0.7
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ ├─┬ iron-validatable-behavior#1.1.2
│ │ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └── polymer#1.9.2
│ │ ├─┬ paper-behaviors#1.0.13
│ │ │ ├─┬ iron-behaviors#1.0.18
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-checked-element-behavior#1.0.6
│ │ │ │ ├─┬ iron-form-element-behavior#1.0.7
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ ├─┬ iron-validatable-behavior#1.1.2
│ │ │ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ paper-ripple#1.0.10
│ │ │ │ ├── iron-a11y-keys-behavior#1.1.9
│ │ │ │ └── polymer#1.9.2
│ │ │ └── polymer#1.9.2
│ │ ├─┬ paper-ripple#1.0.10
│ │ │ ├── iron-a11y-keys-behavior#1.1.9
│ │ │ └── polymer#1.9.2
│ │ ├── paper-styles#1.3.1
│ │ └── polymer#1.9.2
│ ├─┬ paper-dialog#1.1.0 (latest is 2.0.0)
│ │ ├── iron-overlay-behavior#1.10.4 (latest is 2.0.0)
│ │ ├─┬ neon-animation#1.2.5
│ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ ├─┬ iron-resizable-behavior#1.0.6
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-selector#1.5.3
│ │ │ │ └── polymer#1.9.2
│ │ │ ├── polymer#1.9.2
│ │ │ └── web-animations-js#2.2.5
│ │ ├─┬ paper-dialog-behavior#1.2.8
│ │ │ ├─┬ iron-overlay-behavior#1.10.4
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ ├─┬ iron-fit-behavior#1.2.6
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ ├─┬ iron-resizable-behavior#1.0.6
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ └── polymer#1.9.2
│ │ │ ├── paper-styles#1.3.1
│ │ │ └── polymer#1.9.2
│ │ ├─┬ paper-styles#1.3.1
│ │ │ ├── font-roboto#1.0.2
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ └── polymer#1.9.2
│ ├─┬ paper-dialog-behavior#1.2.8 (latest is 2.0.0)
│ │ ├─┬ iron-overlay-behavior#1.10.4
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-fit-behavior#1.2.6
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-resizable-behavior#1.0.6
│ │ │ │ └── polymer#1.9.2
│ │ │ └── polymer#1.9.2
│ │ ├── paper-styles#1.3.1
│ │ └── polymer#1.9.2
│ ├─┬ paper-dialog-scrollable#1.1.5 (latest is 2.1.0)
│ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ └── polymer#1.9.2
│ │ ├─┬ paper-dialog-behavior#1.2.8
│ │ │ ├─┬ iron-overlay-behavior#1.10.4
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ ├─┬ iron-fit-behavior#1.2.6
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ ├─┬ iron-resizable-behavior#1.0.6
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ └── polymer#1.9.2
│ │ │ ├── paper-styles#1.3.1
│ │ │ └── polymer#1.9.2
│ │ ├─┬ paper-styles#1.3.1
│ │ │ ├── font-roboto#1.0.2
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ └─┬ polymer#1.9.2
│ │   └── webcomponentsjs#1.0.1
│ ├─┬ paper-drawer-panel#1.0.11 (latest is 2.0.0)
│ │ ├─┬ iron-media-query#1.0.8
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ ├─┬ iron-resizable-behavior#1.0.6
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-selector#1.5.3
│ │ │ └── polymer#1.9.2
│ │ └── polymer#1.9.2
│ ├─┬ paper-dropdown-menu#1.5.1 (latest is 2.0.0)
│ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-form-element-behavior#1.0.7
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ ├─┬ iron-icon#1.0.13
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-iconset-svg#1.1.1
│ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ ├─┬ iron-validatable-behavior#1.1.2
│ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ ├─┬ paper-behaviors#1.0.13
│ │ │ ├─┬ iron-behaviors#1.0.18
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-checked-element-behavior#1.0.6
│ │ │ │ ├─┬ iron-form-element-behavior#1.0.7
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ ├─┬ iron-validatable-behavior#1.1.2
│ │ │ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ paper-ripple#1.0.10
│ │ │ │ ├── iron-a11y-keys-behavior#1.1.9
│ │ │ │ └── polymer#1.9.2
│ │ │ └── polymer#1.9.2
│ │ ├─┬ paper-input#1.1.24 (latest is 2.0.1)
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-autogrow-textarea#1.0.15
│ │ │ │ ├─┬ iron-behaviors#1.0.18
│ │ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ │ │ │ └── polymer#1.9.2
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ ├─┬ iron-form-element-behavior#1.0.7
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ ├─┬ iron-validatable-behavior#1.1.2
│ │ │ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-behaviors#1.0.18
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-form-element-behavior#1.0.7
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ ├─┬ iron-input#1.0.11
│ │ │ │ ├─┬ iron-a11y-announcer#1.0.6
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ ├─┬ iron-validatable-behavior#1.1.2
│ │ │ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ ├── paper-styles#1.3.1 (latest is 2.0.0)
│ │ │ └── polymer#1.9.2
│ │ ├─┬ paper-menu-button#1.5.2 (latest is 2.0.0)
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-behaviors#1.0.18
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-dropdown#1.5.6
│ │ │ │ ├─┬ iron-behaviors#1.0.18
│ │ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ │ │ │ └── polymer#1.9.2
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ ├── iron-overlay-behavior#1.10.4
│ │ │ │ ├─┬ iron-resizable-behavior#1.0.6
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ ├─┬ neon-animation#1.2.5
│ │ │ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ │ ├─┬ iron-resizable-behavior#1.0.6
│ │ │ │ │ │ └── polymer#1.9.2
│ │ │ │ │ ├─┬ iron-selector#1.5.3
│ │ │ │ │ │ └── polymer#1.9.2
│ │ │ │ │ ├── polymer#1.9.2
│ │ │ │ │ └── web-animations-js#2.2.5
│ │ │ │ └── polymer#1.9.2
│ │ │ ├── iron-fit-behavior#1.2.6 (latest is 2.0.0)
│ │ │ ├─┬ neon-animation#1.2.5
│ │ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ ├─┬ iron-resizable-behavior#1.0.6
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ ├─┬ iron-selector#1.5.3
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ ├── polymer#1.9.2
│ │ │ │ └── web-animations-js#2.2.5
│ │ │ ├─┬ paper-styles#1.3.1
│ │ │ │ ├── font-roboto#1.0.2
│ │ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └── polymer#1.9.2
│ │ ├─┬ paper-ripple#1.0.10
│ │ │ ├── iron-a11y-keys-behavior#1.1.9
│ │ │ └── polymer#1.9.2
│ │ ├─┬ paper-styles#1.3.1
│ │ │ ├── font-roboto#1.0.2
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ └── polymer#1.9.2
│ ├─┬ paper-fab#1.2.2 (latest is 2.0.0)
│ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-icon#1.0.13
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └── polymer#1.9.2
│ │ ├─┬ paper-behaviors#1.0.13
│ │ │ ├─┬ iron-behaviors#1.0.18
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-checked-element-behavior#1.0.6
│ │ │ │ ├─┬ iron-form-element-behavior#1.0.7
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ ├─┬ iron-validatable-behavior#1.1.2
│ │ │ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ paper-ripple#1.0.10
│ │ │ │ ├── iron-a11y-keys-behavior#1.1.9
│ │ │ │ └── polymer#1.9.2
│ │ │ └── polymer#1.9.2
│ │ ├── paper-material#1.0.7 (latest is 2.0.0)
│ │ ├─┬ paper-styles#1.3.1
│ │ │ ├── font-roboto#1.0.2
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ └─┬ polymer#1.9.2
│ │   └── webcomponentsjs#1.0.1
│ ├─┬ paper-header-panel#1.1.7
│ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ └── polymer#1.9.2
│ │ └── polymer#1.9.2
│ ├─┬ paper-icon-button#1.1.6
│ │ ├─┬ iron-icon#1.0.13
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └── polymer#1.9.2
│ │ ├─┬ paper-behaviors#1.0.13
│ │ │ ├─┬ iron-behaviors#1.0.18
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-checked-element-behavior#1.0.6
│ │ │ │ ├─┬ iron-form-element-behavior#1.0.7
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ ├─┬ iron-validatable-behavior#1.1.2
│ │ │ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ paper-ripple#1.0.10
│ │ │ │ ├── iron-a11y-keys-behavior#1.1.9
│ │ │ │ └── polymer#1.9.2
│ │ │ └── polymer#1.9.2
│ │ ├─┬ paper-styles#1.3.1
│ │ │ ├── font-roboto#1.0.2
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ └── polymer#1.9.2
│ ├── paper-input#1.1.24
│ ├─┬ paper-item#1.2.2 (latest is 2.0.0)
│ │ ├─┬ iron-behaviors#1.0.18
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ │ └── polymer#1.9.2
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ └── polymer#1.9.2
│ │ ├─┬ paper-styles#1.3.1
│ │ │ ├── font-roboto#1.0.2
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ └── polymer#1.9.2
│ ├─┬ paper-listbox#1.1.3 (latest is 2.0.0)
│ │ ├─┬ iron-behaviors#1.0.18
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ │ └── polymer#1.9.2
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-collapse#1.3.0
│ │ │ ├─┬ iron-resizable-behavior#1.0.6
│ │ │ │ └── polymer#1.9.2
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-menu-behavior#1.3.1
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-selector#1.5.3
│ │ │ │ └── polymer#1.9.2
│ │ │ └── polymer#1.9.2
│ │ ├─┬ paper-styles#1.3.1
│ │ │ ├── font-roboto#1.0.2
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ └── polymer#1.9.2
│ ├─┬ paper-material#1.0.7
│ │ ├─┬ paper-styles#1.3.1
│ │ │ ├── font-roboto#1.0.2
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ └── polymer#1.9.2
│ ├─┬ paper-menu#1.3.0
│ │ ├─┬ iron-behaviors#1.0.18
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ │ └── polymer#1.9.2
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-collapse#1.3.0
│ │ │ ├─┬ iron-resizable-behavior#1.0.6
│ │ │ │ └── polymer#1.9.2
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-menu-behavior#1.3.1
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-selector#1.5.3
│ │ │ │ └── polymer#1.9.2
│ │ │ └── polymer#1.9.2
│ │ ├─┬ paper-styles#1.3.1
│ │ │ ├── font-roboto#1.0.2
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ └── polymer#1.9.2
│ ├── paper-menu-button#1.5.2 (latest is 2.0.0)
│ ├─┬ paper-progress#1.0.12 (latest is 2.0.1)
│ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-range-behavior#1.0.7
│ │ │ └── polymer#1.9.2
│ │ ├─┬ paper-styles#1.3.1
│ │ │ ├── font-roboto#1.0.2
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ └── polymer#1.9.2
│ ├─┬ paper-radio-button#1.4.0 (latest is 2.0.0)
│ │ ├─┬ iron-checked-element-behavior#1.0.6
│ │ │ ├─┬ iron-form-element-behavior#1.0.7
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ ├─┬ iron-validatable-behavior#1.1.2
│ │ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └── polymer#1.9.2
│ │ ├── iron-flex-layout#1.3.7 (latest is 2.0.0)
│ │ ├─┬ paper-behaviors#1.0.13
│ │ │ ├─┬ iron-behaviors#1.0.18
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-checked-element-behavior#1.0.6
│ │ │ │ ├─┬ iron-form-element-behavior#1.0.7
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ ├─┬ iron-validatable-behavior#1.1.2
│ │ │ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ paper-ripple#1.0.10
│ │ │ │ ├── iron-a11y-keys-behavior#1.1.9
│ │ │ │ └── polymer#1.9.2
│ │ │ └── polymer#1.9.2
│ │ ├── paper-styles#1.3.1
│ │ └── polymer#1.9.2
│ ├─┬ paper-radio-group#1.2.2 (latest is 2.0.0)
│ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ └── polymer#1.9.2
│ │ ├── iron-menu-behavior#1.3.1 (latest is 2.0.0)
│ │ ├─┬ paper-radio-button#1.4.0
│ │ │ ├─┬ iron-checked-element-behavior#1.0.6
│ │ │ │ ├─┬ iron-form-element-behavior#1.0.7
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ ├─┬ iron-validatable-behavior#1.1.2
│ │ │ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ └── polymer#1.9.2
│ │ │ ├── iron-flex-layout#1.3.7
│ │ │ ├─┬ paper-behaviors#1.0.13
│ │ │ │ ├─┬ iron-behaviors#1.0.18
│ │ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ │ │ │ └── polymer#1.9.2
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ ├─┬ iron-checked-element-behavior#1.0.6
│ │ │ │ │ ├─┬ iron-form-element-behavior#1.0.7
│ │ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ │ ├─┬ iron-validatable-behavior#1.1.2
│ │ │ │ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ ├─┬ paper-ripple#1.0.10
│ │ │ │ │ ├── iron-a11y-keys-behavior#1.1.9
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ └── polymer#1.9.2
│ │ │ ├── paper-styles#1.3.1
│ │ │ └── polymer#1.9.2
│ │ └── polymer#1.9.2
│ ├─┬ paper-ripple#1.0.10
│ │ ├── iron-a11y-keys-behavior#1.1.9
│ │ └── polymer#1.9.2
│ ├─┬ paper-scroll-header-panel#1.0.16 (latest is 2.0.0)
│ │ ├─┬ iron-resizable-behavior#1.0.6
│ │ │ └── polymer#1.9.2
│ │ └── polymer#1.9.2
│ ├─┬ paper-slider#1.0.15 (latest is 2.0.1)
│ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-behaviors#1.0.18
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ │ └── polymer#1.9.2
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-form-element-behavior#1.0.7
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ ├─┬ paper-behaviors#1.0.13
│ │ │ ├─┬ iron-behaviors#1.0.18
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-checked-element-behavior#1.0.6
│ │ │ │ ├─┬ iron-form-element-behavior#1.0.7
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ ├─┬ iron-validatable-behavior#1.1.2
│ │ │ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ paper-ripple#1.0.10
│ │ │ │ ├── iron-a11y-keys-behavior#1.1.9
│ │ │ │ └── polymer#1.9.2
│ │ │ └── polymer#1.9.2
│ │ ├── paper-input#1.1.24
│ │ ├─┬ paper-progress#1.0.12
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-range-behavior#1.0.7
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ paper-styles#1.3.1
│ │ │ │ ├── font-roboto#1.0.2
│ │ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └── polymer#1.9.2
│ │ ├─┬ paper-styles#1.3.1
│ │ │ ├── font-roboto#1.0.2
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ └── polymer#1.9.2
│ ├─┬ paper-spinner#1.2.1 (latest is 2.0.0)
│ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ └── polymer#1.9.2
│ │ ├─┬ paper-styles#1.3.1
│ │ │ ├── font-roboto#1.0.2
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ └── polymer#1.9.2
│ ├─┬ paper-styles#1.3.1
│ │ ├── font-roboto#1.0.2
│ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ └── polymer#1.9.2
│ │ └─┬ polymer#1.9.2
│ │   └── webcomponentsjs#1.0.1
│ ├─┬ paper-tabs#1.8.0 (latest is 2.0.0)
│ │ ├─┬ iron-behaviors#1.0.18
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ │ └── polymer#1.9.2
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-icon#1.0.13
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └── polymer#1.9.2
│ │ ├─┬ iron-iconset-svg#1.1.1
│ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ ├── iron-menu-behavior#1.3.1 (latest is 2.0.0)
│ │ ├─┬ iron-resizable-behavior#1.0.6
│ │ │ └── polymer#1.9.2
│ │ ├─┬ paper-behaviors#1.0.13
│ │ │ ├─┬ iron-behaviors#1.0.18
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-checked-element-behavior#1.0.6
│ │ │ │ ├─┬ iron-form-element-behavior#1.0.7
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ ├─┬ iron-validatable-behavior#1.1.2
│ │ │ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ paper-ripple#1.0.10
│ │ │ │ ├── iron-a11y-keys-behavior#1.1.9
│ │ │ │ └── polymer#1.9.2
│ │ │ └── polymer#1.9.2
│ │ ├─┬ paper-icon-button#1.1.6
│ │ │ ├─┬ iron-icon#1.0.13
│ │ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ paper-behaviors#1.0.13
│ │ │ │ ├─┬ iron-behaviors#1.0.18
│ │ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ │ │ │ └── polymer#1.9.2
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ ├─┬ iron-checked-element-behavior#1.0.6
│ │ │ │ │ ├─┬ iron-form-element-behavior#1.0.7
│ │ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ │ ├─┬ iron-validatable-behavior#1.1.2
│ │ │ │ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ ├─┬ paper-ripple#1.0.10
│ │ │ │ │ ├── iron-a11y-keys-behavior#1.1.9
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ paper-styles#1.3.1
│ │ │ │ ├── font-roboto#1.0.2
│ │ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └── polymer#1.9.2
│ │ ├─┬ paper-styles#1.3.1
│ │ │ ├── font-roboto#1.0.2
│ │ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ │ └── polymer#1.9.2
│ │ │ └─┬ polymer#1.9.2
│ │ │   └── webcomponentsjs#1.0.1
│ │ └── polymer#1.9.2
│ ├─┬ paper-toast#1.3.1 (latest is 2.0.0)
│ │ ├─┬ iron-a11y-announcer#1.0.6
│ │ │ └── polymer#1.9.2
│ │ ├── iron-fit-behavior#1.2.6 (latest is 2.0.0)
│ │ ├── iron-overlay-behavior#1.10.4 (latest is 2.0.0)
│ │ └── polymer#1.9.2
│ ├─┬ paper-toggle-button#1.3.0 (latest is 2.0.0)
│ │ ├─┬ iron-checked-element-behavior#1.0.6
│ │ │ ├─┬ iron-form-element-behavior#1.0.7
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ ├─┬ iron-validatable-behavior#1.1.2
│ │ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ └─┬ polymer#1.9.2
│ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ └── polymer#1.9.2
│ │ ├─┬ paper-behaviors#1.0.13
│ │ │ ├─┬ iron-behaviors#1.0.18
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.9
│ │ │ │ │ └── polymer#1.9.2
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ iron-checked-element-behavior#1.0.6
│ │ │ │ ├─┬ iron-form-element-behavior#1.0.7
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ ├─┬ iron-validatable-behavior#1.1.2
│ │ │ │ │ ├─┬ iron-meta#1.1.3
│ │ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ │ └─┬ polymer#1.9.2
│ │ │ │ │   └── webcomponentsjs#1.0.1
│ │ │ │ └── polymer#1.9.2
│ │ │ ├─┬ paper-ripple#1.0.10
│ │ │ │ ├── iron-a11y-keys-behavior#1.1.9
│ │ │ │ └── polymer#1.9.2
│ │ │ └── polymer#1.9.2
│ │ ├── paper-styles#1.3.1
│ │ └── polymer#1.9.2
│ ├─┬ paper-toolbar#1.1.7
│ │ ├─┬ iron-flex-layout#1.3.7
│ │ │ └── polymer#1.9.2
│ │ ├── paper-styles#1.3.1
│ │ └── polymer#1.9.2
│ └─┬ paper-tooltip#1.1.4 (latest is 2.0.0)
│   ├─┬ neon-animation#1.2.5
│   │ ├─┬ iron-meta#1.1.3
│   │ │ └─┬ polymer#1.9.2
│   │ │   └── webcomponentsjs#1.0.1
│   │ ├─┬ iron-resizable-behavior#1.0.6
│   │ │ └── polymer#1.9.2
│   │ ├─┬ iron-selector#1.5.3
│   │ │ └── polymer#1.9.2
│   │ ├── polymer#1.9.2
│   │ └── web-animations-js#2.2.5
│   ├─┬ paper-styles#1.3.1
│   │ ├── font-roboto#1.0.2
│   │ ├─┬ iron-flex-layout#1.3.7
│   │ │ └── polymer#1.9.2
│   │ └─┬ polymer#1.9.2
│   │   └── webcomponentsjs#1.0.1
│   └── polymer#1.9.2
├─┬ platinum-elements#2.0.0
│ ├─┬ platinum-bluetooth#2.1.2
│ │ ├─┬ polymer#1.9.2
│ │ │ └── webcomponentsjs#1.0.1
│ │ └─┬ promise-polyfill#1.0.1
│ │   └─┬ polymer#1.9.2
│ │     └── webcomponentsjs#1.0.1
│ ├─┬ platinum-https-redirect#1.0.2
│ │ └── polymer#1.9.2
│ ├─┬ platinum-push-messaging#1.0.5
│ │ ├─┬ polymer#1.9.2
│ │ │ └── webcomponentsjs#1.0.1
│ │ └─┬ promise-polyfill#1.0.1
│ │   └─┬ polymer#1.9.2
│ │     └── webcomponentsjs#1.0.1
│ └─┬ platinum-sw#1.3.0
│   ├─┬ polymer#1.9.2
│   │ └── webcomponentsjs#1.0.1
│   └── sw-toolbox#3.6.1
├─┬ polymer#1.9.2 (2.0.1 available)
│ └── webcomponentsjs#1.0.1
├── polymerfire#0.9.7 (2.1.0 available)
└── shadycss#1.0.1 extraneous
```
