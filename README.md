# polymer-cdn <sup><sub>v1.5.0</sub></sup>
**A mirror of Polymer's components so that they can be used directly from CDN**

![Polymer CDN is powered by MaxCDN](http://i.imgur.com/9obTXpk.png)

## How to use
In general, given an element named `my-cool-element`, the CDN url for it will be:
```
https://cdn.rawgit.com/download/polymer-cdn/1.5.0/lib/my-cool-element/my-cool-element.html
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

Pull requests are of course also always welcome! If you want to try that, here is the rough procedure:
 1.  Create an issue in this repo describing your change and mention you're preparing a pull request
 2.  Fork this repo
 3.  Clone your forked repo to your own machine
 4.  Create and switch to a new Branch
 5.  Implement the change
 6.  Commit your change, making sure to mention the URL to the issue created in step 1 in the commit comment
 7.  Push your change to your fork (make sure to push the right branch)
 8.  Create a Pull Request from your change.

I will review the PR and if it looks good, Merge it and Publish the resulting work as a new Release.

## Contents
All the libraries available in polymer-cdn can be found side-by-side in the [lib](https://github.com/Download/polymer-cdn/tree/1.5.0/lib) subfolder.

Some of the libraries depend on other libraries. We call those other libraries the dependencies of the library.
These dependencies will also be pulled into your page when you include such a library.
If the dependencies themselves depend on yet other libraries, these dependencies of dependencies will also be
pulled into your page, et cetera until the full dependency tree has been loaded. We call this transitive
dependency resolution and it's built in to the way Web Components work.

The bower output below lists, for each library included in this CDN, the dependencies of that library.
These dependencies are themselves also listed at the top-level, so you can work out the entire dependency
tree for a library by carefully examining this diagram.

```sh
polymer-cdn#1.5.0
├─┬ app-elements#0.9.0
│ ├─┬ app-layout#0.9.1
│ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-media-query#1.0.8
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-scroll-target-behavior#1.0.6
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ app-localize-behavior#0.9.1
│ │ ├── intl-messageformat#1.3.0
│ │ ├─┬ iron-ajax#1.2.0
│ │ │ ├── polymer#1.5.0
│ │ │ └─┬ promise-polyfill#1.0.0
│ │ │   └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ app-pouchdb#0.9.1
│ │ ├─┬ app-storage#0.9.3
│ │ │ ├── polymer#1.5.0
│ │ │ └─┬ promise-polyfill#1.0.0
│ │ │   └── polymer#1.5.0
│ │ ├── polymer#1.5.0
│ │ ├── pouchdb#5.4.1
│ │ ├── pouchdb-find#0.9.0 (latest is 0.10.0)
│ │ └─┬ promise-polyfill#1.0.0
│ │   └── polymer#1.5.0
│ ├─┬ app-route#0.9.1
│ │ ├── iron-location#0.8.3
│ │ └── polymer#1.5.0
│ └── app-storage#0.9.3
├─┬ carbon-elements#0.1.0 extraneous
│ └─┬ carbon-route#0.8.5 extraneous (latest is 0.9.1)
│   ├─┬ iron-location#0.8.3
│   │ └── polymer#1.5.0
│   └─┬ polymer#1.5.0
│     └── webcomponentsjs#0.7.22
├─┬ carbon-route#0.8.5 extraneous (latest is 0.9.1)
│ ├─┬ iron-location#0.8.3
│ │ └── polymer#1.5.0
│ └─┬ polymer#1.5.0
│   └── webcomponentsjs#0.7.22
├─┬ gold-elements#1.0.1
│ ├─┬ gold-cc-cvc-input#1.0.9
│ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-icon#1.0.8
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├── paper-input#1.1.11
│ │ ├─┬ paper-styles#1.1.4
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ gold-cc-expiration-input#1.1.2
│ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-validatable-behavior#1.1.1
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-validator-behavior#1.0.1
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├── paper-input#1.1.11
│ │ ├─┬ paper-styles#1.1.4
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ gold-cc-input#1.0.7
│ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-icon#1.0.8
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-validator-behavior#1.0.1
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├── paper-input#1.1.11
│ │ ├─┬ paper-styles#1.1.4
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ gold-email-input#1.0.7
│ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-icon#1.0.8
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├── paper-input#1.1.11
│ │ ├─┬ paper-styles#1.1.4
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ gold-phone-input#1.0.9
│ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-input#1.0.10
│ │ │ ├─┬ iron-a11y-announcer#1.0.4
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-validatable-behavior#1.1.1
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├── paper-input#1.1.11
│ │ ├─┬ paper-styles#1.1.4
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ └─┬ gold-zip-input#1.0.5
│   ├─┬ iron-form-element-behavior#1.0.6
│   │ └── polymer#1.5.0
│   ├─┬ iron-icon#1.0.8
│   │ ├─┬ iron-flex-layout#1.3.1
│   │ │ └── polymer#1.5.0
│   │ ├─┬ iron-meta#1.1.1
│   │ │ └── polymer#1.5.0
│   │ └── polymer#1.5.0
│   ├─┬ iron-validator-behavior#1.0.1
│   │ ├─┬ iron-meta#1.1.1
│   │ │ └── polymer#1.5.0
│   │ └── polymer#1.5.0
│   ├── paper-input#1.1.11
│   ├─┬ paper-styles#1.1.4
│   │ ├── font-roboto#1.0.1
│   │ ├─┬ iron-flex-layout#1.3.1
│   │ │ └── polymer#1.5.0
│   │ └── polymer#1.5.0
│   └── polymer#1.5.0
├─┬ google-web-components#1.1.0
│ ├─┬ firebase-element#1.0.14
│ │ ├── firebase#2.4.2 (latest is 3.0.4)
│ │ └── polymer#1.5.0
│ ├─┬ google-analytics#1.2.1
│ │ ├── ga-api-utils#0.2.0 (latest is 0.5.0)
│ │ ├─┬ google-chart#1.0.5
│ │ │ ├─┬ google-apis#1.1.5
│ │ │ │ ├─┬ iron-jsonp-library#1.0.4
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-ajax#1.2.0
│ │ │ │ ├── polymer#1.5.0
│ │ │ │ └─┬ promise-polyfill#1.0.0
│ │ │ │   └── polymer#1.5.0
│ │ │ ├── polymer#1.5.0
│ │ │ └─┬ promise-polyfill#1.0.0
│ │ │   └── polymer#1.5.0
│ │ ├─┬ google-signin#1.3.4
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ google-apis#1.1.5
│ │ │ │ ├─┬ iron-jsonp-library#1.0.4
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├── iron-flex-layout#1.3.1
│ │ │ ├─┬ iron-icon#1.0.8
│ │ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-iconset-svg#1.0.9
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ paper-material#1.0.6
│ │ │ │ ├─┬ paper-styles#1.1.4
│ │ │ │ │ ├── font-roboto#1.0.1
│ │ │ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ paper-ripple#1.0.5
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├── polymer#1.5.0
│ │ └─┬ promise-polyfill#1.0.0
│ │   └── polymer#1.5.0
│ ├─┬ google-apis#1.1.5
│ │ ├─┬ iron-jsonp-library#1.0.4
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ google-calendar#1.0.1
│ │ ├── google-apis#1.1.5
│ │ ├── google-signin#1.3.4
│ │ └── polymer#1.5.0
│ ├─┬ google-castable-video#1.0.2
│ │ └── polymer#1.5.0
│ ├─┬ google-chart#1.0.5
│ │ ├─┬ google-apis#1.1.5
│ │ │ ├─┬ iron-jsonp-library#1.0.4
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-ajax#1.2.0
│ │ │ ├── polymer#1.5.0
│ │ │ └─┬ promise-polyfill#1.0.0
│ │ │   └── polymer#1.5.0
│ │ ├── polymer#1.5.0
│ │ └─┬ promise-polyfill#1.0.0
│ │   └── polymer#1.5.0
│ ├─┬ google-feeds#1.0.2
│ │ ├── google-apis#1.1.5
│ │ ├─┬ iron-jsonp-library#1.0.4
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ google-hangout-button#1.0.1
│ │ ├─┬ google-apis#1.1.5
│ │ │ ├─┬ iron-jsonp-library#1.0.4
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ google-map#1.1.10
│ │ ├── google-apis#1.1.5
│ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ └── polymer#1.5.0
│ │ ├── iron-selector#1.5.2
│ │ └── polymer#1.5.0
│ ├─┬ google-sheets#1.0.5
│ │ ├── google-apis#1.1.5
│ │ ├── google-signin#1.3.4
│ │ ├─┬ iron-ajax#1.2.0
│ │ │ ├── polymer#1.5.0
│ │ │ └─┬ promise-polyfill#1.0.0
│ │ │   └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ google-signin#1.3.4
│ │ ├── font-roboto#1.0.1
│ │ ├─┬ google-apis#1.1.5
│ │ │ ├─┬ iron-jsonp-library#1.0.4
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├── iron-flex-layout#1.3.1
│ │ ├─┬ iron-icon#1.0.8
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-iconset-svg#1.0.9
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-material#1.0.6
│ │ │ ├─┬ paper-styles#1.1.4
│ │ │ │ ├── font-roboto#1.0.1
│ │ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-ripple#1.0.5
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ google-streetview-pano#1.0.3
│ │ ├── google-apis#1.1.5
│ │ └── polymer#1.5.0
│ ├─┬ google-url-shortener#1.0.1
│ │ ├─┬ google-apis#1.1.5
│ │ │ ├─┬ iron-jsonp-library#1.0.4
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ google-youtube#1.2.1
│ │ ├─┬ google-apis#1.1.5
│ │ │ ├─┬ iron-jsonp-library#1.0.4
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-localstorage#1.0.5
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ google-youtube-upload#1.1.2 (latest is 2.0.0)
│ │ ├── cors-upload-sample#37c97848a2
│ │ ├─┬ google-signin#1.3.4
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ google-apis#1.1.5
│ │ │ │ ├─┬ iron-jsonp-library#1.0.4
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├── iron-flex-layout#1.3.1
│ │ │ ├─┬ iron-icon#1.0.8
│ │ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-iconset-svg#1.0.9
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ paper-material#1.0.6
│ │ │ │ ├─┬ paper-styles#1.1.4
│ │ │ │ │ ├── font-roboto#1.0.1
│ │ │ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ paper-ripple#1.0.5
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ └─┬ polymerfire#0.9.2
│   ├── app-storage#0.9.3
│   ├── firebase-sdk
│   └── polymer#1.5.0
├─┬ iron-elements#1.0.10
│ ├─┬ iron-a11y-announcer#1.0.4
│ │ └── polymer#1.5.0
│ ├─┬ iron-a11y-keys#1.0.5
│ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ └── polymer#1.5.0
│ ├─┬ iron-ajax#1.2.0
│ │ ├── polymer#1.5.0
│ │ └─┬ promise-polyfill#1.0.0
│ │   └── polymer#1.5.0
│ ├─┬ iron-autogrow-textarea#1.0.12
│ │ ├─┬ iron-behaviors#1.0.16
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-validatable-behavior#1.1.1
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ iron-behaviors#1.0.16
│ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ iron-checked-element-behavior#1.0.4
│ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-validatable-behavior#1.1.1
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ iron-collapse#1.1.0
│ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ iron-component-page#1.1.6
│ │ ├── hydrolysis#1.24.0
│ │ ├─┬ iron-ajax#1.2.0
│ │ │ ├── polymer#1.5.0
│ │ │ └─┬ promise-polyfill#1.0.0
│ │ │   └── polymer#1.5.0
│ │ ├─┬ iron-doc-viewer#1.0.14
│ │ │ ├─┬ marked-element#1.1.3
│ │ │ │ ├── marked#0.3.5
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ paper-button#1.0.12
│ │ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ paper-behaviors#1.0.11
│ │ │ │ │ ├─┬ iron-behaviors#1.0.16
│ │ │ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ ├─┬ iron-checked-element-behavior#1.0.4
│ │ │ │ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ │ ├─┬ iron-validatable-behavior#1.1.1
│ │ │ │ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ ├─┬ paper-ripple#1.0.5
│ │ │ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ paper-material#1.0.6
│ │ │ │ │ ├─┬ paper-styles#1.1.4
│ │ │ │ │ │ ├── font-roboto#1.0.1
│ │ │ │ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ paper-styles#1.1.4
│ │ │ │ ├── font-roboto#1.0.1
│ │ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├── polymer#1.5.0
│ │ │ └─┬ prism-element#1.1.0
│ │ │   ├── polymer#1.5.0
│ │ │   └── prism#1.5.1
│ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-icons#1.1.3
│ │ │ ├─┬ iron-icon#1.0.8
│ │ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-iconset-svg#1.0.9
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-selector#1.5.2
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-header-panel#1.1.6
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-styles#1.1.4
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-toolbar#1.1.4
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ ├── paper-styles#1.1.4
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ iron-demo-helpers#1.2.3
│ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-icons#1.1.3
│ │ │ ├─┬ iron-icon#1.0.8
│ │ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-iconset-svg#1.0.9
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-location#0.8.3
│ │ │ └── polymer#1.5.0
│ │ ├─┬ marked-element#1.1.3
│ │ │ ├── marked#0.3.5
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-icon-button#1.1.1
│ │ │ ├─┬ iron-icon#1.0.8
│ │ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ paper-behaviors#1.0.11
│ │ │ │ ├─┬ iron-behaviors#1.0.16
│ │ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-checked-element-behavior#1.0.4
│ │ │ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ ├─┬ iron-validatable-behavior#1.1.1
│ │ │ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ paper-ripple#1.0.5
│ │ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ paper-styles#1.1.4
│ │ │ │ ├── font-roboto#1.0.1
│ │ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-styles#1.1.4
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├── polymer#1.5.0
│ │ └── prism-element#1.1.0
│ ├── iron-doc-viewer#1.0.14
│ ├─┬ iron-dropdown#1.4.1
│ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-behaviors#1.0.16
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-overlay-behavior#1.8.0
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-fit-behavior#1.2.2
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ └── polymer#1.5.0
│ │ ├─┬ neon-animation#1.2.3
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-selector#1.5.2
│ │ │ │ └── polymer#1.5.0
│ │ │ ├── polymer#1.5.0
│ │ │ └── web-animations-js#2.2.1
│ │ └── polymer#1.5.0
│ ├─┬ iron-fit-behavior#1.2.2
│ │ └── polymer#1.5.0
│ ├─┬ iron-flex-layout#1.3.1
│ │ └── polymer#1.5.0
│ ├─┬ iron-form#1.0.16
│ │ ├─┬ iron-ajax#1.2.0
│ │ │ ├── polymer#1.5.0
│ │ │ └─┬ promise-polyfill#1.0.0
│ │ │   └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ iron-form-element-behavior#1.0.6
│ │ └── polymer#1.5.0
│ ├─┬ iron-icon#1.0.8
│ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-meta#1.1.1
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ iron-icons#1.1.3
│ │ ├─┬ iron-icon#1.0.8
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-iconset-svg#1.0.9
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ iron-iconset#1.0.4
│ │ ├─┬ iron-meta#1.1.1
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ iron-iconset-svg#1.0.9
│ │ ├─┬ iron-meta#1.1.1
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├── iron-image#1.2.3
│ ├─┬ iron-input#1.0.10
│ │ ├─┬ iron-a11y-announcer#1.0.4
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-validatable-behavior#1.1.1
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ iron-jsonp-library#1.0.4
│ │ └── polymer#1.5.0
│ ├─┬ iron-label#1.0.2
│ │ └── polymer#1.5.0
│ ├─┬ iron-list#1.3.2
│ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-scroll-target-behavior#1.0.6
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ iron-localstorage#1.0.5
│ │ └── polymer#1.5.0
│ ├─┬ iron-location#0.8.3
│ │ └── polymer#1.5.0
│ ├─┬ iron-media-query#1.0.8
│ │ └── polymer#1.5.0
│ ├─┬ iron-menu-behavior#1.1.7
│ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-selector#1.5.2
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ iron-meta#1.1.1
│ │ └── polymer#1.5.0
│ ├─┬ iron-overlay-behavior#1.8.0
│ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-fit-behavior#1.2.2
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ iron-pages#1.0.7
│ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-selector#1.5.2
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ iron-range-behavior#1.0.5
│ │ └── polymer#1.5.0
│ ├─┬ iron-resizable-behavior#1.0.3
│ │ └── polymer#1.5.0
│ ├─┬ iron-scroll-target-behavior#1.0.6
│ │ └── polymer#1.5.0
│ ├─┬ iron-scroll-threshold#1.0.1
│ │ ├─┬ iron-scroll-target-behavior#1.0.6
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ iron-selector#1.5.2
│ │ └── polymer#1.5.0
│ ├─┬ iron-signals#1.0.3
│ │ └── polymer#1.5.0
│ ├─┬ iron-swipeable-container#1.0.2
│ │ └── polymer#1.5.0
│ ├─┬ iron-test-helpers#1.2.5
│ │ └── polymer#1.5.0
│ ├─┬ iron-validatable-behavior#1.1.1
│ │ ├─┬ iron-meta#1.1.1
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ └─┬ iron-validator-behavior#1.0.1
│   ├─┬ iron-meta#1.1.1
│   │ └── polymer#1.5.0
│   └── polymer#1.5.0
├─┬ iron-page-url#0.7.3 extraneous (latest is 0.8.3)
│ └─┬ polymer#1.5.0
│   └── webcomponentsjs#0.7.22
├─┬ molecules#1.0.0
│ └─┬ marked-element#1.1.3
│   ├── marked#0.3.5
│   └── polymer#1.5.0
├─┬ neon-elements#1.0.0
│ └─┬ neon-animation#1.2.3
│   ├─┬ iron-meta#1.1.1
│   │ └── polymer#1.5.0
│   ├─┬ iron-resizable-behavior#1.0.3
│   │ └── polymer#1.5.0
│   ├─┬ iron-selector#1.5.2
│   │ └── polymer#1.5.0
│   ├── polymer#1.5.0
│   └── web-animations-js#2.2.1
├─┬ paper-elements#1.0.7
│ ├─┬ paper-badge#1.1.1
│ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-styles#1.1.4
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ paper-behaviors#1.0.11
│ │ ├─┬ iron-behaviors#1.0.16
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-checked-element-behavior#1.0.4
│ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-validatable-behavior#1.1.1
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-ripple#1.0.5
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ paper-button#1.0.12
│ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-behaviors#1.0.11
│ │ │ ├─┬ iron-behaviors#1.0.16
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-checked-element-behavior#1.0.4
│ │ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-validatable-behavior#1.1.1
│ │ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ paper-ripple#1.0.5
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-material#1.0.6
│ │ │ ├─┬ paper-styles#1.1.4
│ │ │ │ ├── font-roboto#1.0.1
│ │ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ paper-card#1.1.1
│ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-image#1.2.3
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-material#1.0.6
│ │ │ ├─┬ paper-styles#1.1.4
│ │ │ │ ├── font-roboto#1.0.1
│ │ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├── paper-styles#1.1.4
│ │ └── polymer#1.5.0
│ ├─┬ paper-checkbox#1.2.0
│ │ ├─┬ iron-checked-element-behavior#1.0.4
│ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-validatable-behavior#1.1.1
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-behaviors#1.0.11
│ │ │ ├─┬ iron-behaviors#1.0.16
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-checked-element-behavior#1.0.4
│ │ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-validatable-behavior#1.1.1
│ │ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ paper-ripple#1.0.5
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-ripple#1.0.5
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├── paper-styles#1.1.4
│ │ └── polymer#1.5.0
│ ├─┬ paper-dialog#1.0.4
│ │ ├─┬ neon-animation#1.2.3
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-selector#1.5.2
│ │ │ │ └── polymer#1.5.0
│ │ │ ├── polymer#1.5.0
│ │ │ └── web-animations-js#2.2.1
│ │ ├─┬ paper-dialog-behavior#1.2.6
│ │ │ ├─┬ iron-overlay-behavior#1.8.0
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-fit-behavior#1.2.2
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├── paper-styles#1.1.4
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-styles#1.1.4
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ paper-dialog-behavior#1.2.6
│ │ ├─┬ iron-overlay-behavior#1.8.0
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-fit-behavior#1.2.2
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├── paper-styles#1.1.4
│ │ └── polymer#1.5.0
│ ├─┬ paper-dialog-scrollable#1.1.4
│ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-dialog-behavior#1.2.6
│ │ │ ├─┬ iron-overlay-behavior#1.8.0
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-fit-behavior#1.2.2
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├── paper-styles#1.1.4
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-styles#1.1.4
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ paper-drawer-panel#1.0.9
│ │ ├─┬ iron-media-query#1.0.8
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-selector#1.5.2
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ paper-dropdown-menu#1.2.1
│ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-icon#1.0.8
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-iconset-svg#1.0.9
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-validatable-behavior#1.1.1
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-behaviors#1.0.11
│ │ │ ├─┬ iron-behaviors#1.0.16
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-checked-element-behavior#1.0.4
│ │ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-validatable-behavior#1.1.1
│ │ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ paper-ripple#1.0.5
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-input#1.1.11
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-autogrow-textarea#1.0.12
│ │ │ │ ├─┬ iron-behaviors#1.0.16
│ │ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-validatable-behavior#1.1.1
│ │ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-behaviors#1.0.16
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-input#1.0.10
│ │ │ │ ├─┬ iron-a11y-announcer#1.0.4
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-validatable-behavior#1.1.1
│ │ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├── paper-styles#1.1.4
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-menu-button#1.1.0
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-behaviors#1.0.16
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-dropdown#1.4.1
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-behaviors#1.0.16
│ │ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-overlay-behavior#1.8.0
│ │ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ ├─┬ iron-fit-behavior#1.2.2
│ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ neon-animation#1.2.3
│ │ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ ├─┬ iron-selector#1.5.2
│ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ ├── polymer#1.5.0
│ │ │ │ │ └── web-animations-js#2.2.1
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ neon-animation#1.2.3
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-selector#1.5.2
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├── polymer#1.5.0
│ │ │ │ └── web-animations-js#2.2.1
│ │ │ ├─┬ paper-styles#1.1.4
│ │ │ │ ├── font-roboto#1.0.1
│ │ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-ripple#1.0.5
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-styles#1.1.4
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ paper-fab#1.2.0
│ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-icon#1.0.8
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-icons#1.1.3
│ │ │ ├─┬ iron-icon#1.0.8
│ │ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-iconset-svg#1.0.9
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-behaviors#1.0.11
│ │ │ ├─┬ iron-behaviors#1.0.16
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-checked-element-behavior#1.0.4
│ │ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-validatable-behavior#1.1.1
│ │ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ paper-ripple#1.0.5
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├── paper-material#1.0.6
│ │ ├─┬ paper-styles#1.1.4
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ paper-header-panel#1.1.6
│ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ paper-icon-button#1.1.1
│ │ ├─┬ iron-icon#1.0.8
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-behaviors#1.0.11
│ │ │ ├─┬ iron-behaviors#1.0.16
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-checked-element-behavior#1.0.4
│ │ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-validatable-behavior#1.1.1
│ │ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ paper-ripple#1.0.5
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-styles#1.1.4
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├── paper-input#1.1.11
│ ├─┬ paper-item#1.2.1
│ │ ├─┬ iron-behaviors#1.0.16
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-styles#1.1.4
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ paper-listbox#1.1.2
│ │ ├─┬ iron-behaviors#1.0.16
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-collapse#1.1.0
│ │ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-menu-behavior#1.1.7
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-selector#1.5.2
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-styles#1.1.4
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ paper-material#1.0.6
│ │ ├─┬ paper-styles#1.1.4
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ paper-menu#1.2.2
│ │ ├─┬ iron-behaviors#1.0.16
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-collapse#1.1.0
│ │ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-menu-behavior#1.1.7
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-selector#1.5.2
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-styles#1.1.4
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ paper-menu-button#1.1.0
│ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-behaviors#1.0.16
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-dropdown#1.4.1
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-behaviors#1.0.16
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-overlay-behavior#1.8.0
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-fit-behavior#1.2.2
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ neon-animation#1.2.3
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-selector#1.5.2
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├── polymer#1.5.0
│ │ │ │ └── web-animations-js#2.2.1
│ │ │ └── polymer#1.5.0
│ │ ├─┬ neon-animation#1.2.3
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-selector#1.5.2
│ │ │ │ └── polymer#1.5.0
│ │ │ ├── polymer#1.5.0
│ │ │ └── web-animations-js#2.2.1
│ │ ├─┬ paper-styles#1.1.4
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ paper-progress#1.0.9
│ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-range-behavior#1.0.5
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-styles#1.1.4
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ paper-radio-button#1.2.0
│ │ ├─┬ iron-checked-element-behavior#1.0.4
│ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-validatable-behavior#1.1.1
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├── iron-flex-layout#1.3.1
│ │ ├─┬ paper-behaviors#1.0.11
│ │ │ ├─┬ iron-behaviors#1.0.16
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-checked-element-behavior#1.0.4
│ │ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-validatable-behavior#1.1.1
│ │ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ paper-ripple#1.0.5
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├── paper-styles#1.1.4
│ │ └── polymer#1.5.0
│ ├─┬ paper-radio-group#1.2.0
│ │ ├── iron-menu-behavior#1.1.7
│ │ └── polymer#1.5.0
│ ├─┬ paper-ripple#1.0.5
│ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ paper-scroll-header-panel#1.0.15
│ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ paper-slider#1.0.11
│ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-behaviors#1.0.16
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-behaviors#1.0.11
│ │ │ ├─┬ iron-behaviors#1.0.16
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-checked-element-behavior#1.0.4
│ │ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-validatable-behavior#1.1.1
│ │ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ paper-ripple#1.0.5
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├── paper-input#1.1.11
│ │ ├─┬ paper-progress#1.0.9
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-range-behavior#1.0.5
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ paper-styles#1.1.4
│ │ │ │ ├── font-roboto#1.0.1
│ │ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-styles#1.1.4
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ paper-spinner#1.2.0
│ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-styles#1.1.4
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ paper-styles#1.1.4
│ │ ├── font-roboto#1.0.1
│ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ paper-tabs#1.6.0
│ │ ├─┬ iron-behaviors#1.0.16
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-icon#1.0.8
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ iron-iconset-svg#1.0.9
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├── iron-menu-behavior#1.1.7
│ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-behaviors#1.0.11
│ │ │ ├─┬ iron-behaviors#1.0.16
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-checked-element-behavior#1.0.4
│ │ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-validatable-behavior#1.1.1
│ │ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ paper-ripple#1.0.5
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-icon-button#1.1.1
│ │ │ ├─┬ iron-icon#1.0.8
│ │ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ paper-behaviors#1.0.11
│ │ │ │ ├─┬ iron-behaviors#1.0.16
│ │ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-checked-element-behavior#1.0.4
│ │ │ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ ├─┬ iron-validatable-behavior#1.1.1
│ │ │ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ paper-ripple#1.0.5
│ │ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ paper-styles#1.1.4
│ │ │ │ ├── font-roboto#1.0.1
│ │ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-styles#1.1.4
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ └── polymer#1.5.0
│ ├─┬ paper-toast#1.3.0
│ │ ├─┬ iron-a11y-announcer#1.0.4
│ │ │ └── polymer#1.5.0
│ │ ├── iron-fit-behavior#1.2.2
│ │ ├── iron-overlay-behavior#1.8.0
│ │ └── polymer#1.5.0
│ ├─┬ paper-toggle-button#1.1.2
│ │ ├─┬ iron-checked-element-behavior#1.0.4
│ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-validatable-behavior#1.1.1
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├─┬ paper-behaviors#1.0.11
│ │ │ ├─┬ iron-behaviors#1.0.16
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ iron-checked-element-behavior#1.0.4
│ │ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ ├─┬ iron-validatable-behavior#1.1.1
│ │ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ │ └── polymer#1.5.0
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ ├─┬ paper-ripple#1.0.5
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.3
│ │ │ │ │ └── polymer#1.5.0
│ │ │ │ └── polymer#1.5.0
│ │ │ └── polymer#1.5.0
│ │ ├── paper-styles#1.1.4
│ │ └── polymer#1.5.0
│ ├─┬ paper-toolbar#1.1.4
│ │ ├─┬ iron-flex-layout#1.3.1
│ │ │ └── polymer#1.5.0
│ │ ├── paper-styles#1.1.4
│ │ └── polymer#1.5.0
│ └─┬ paper-tooltip#1.1.2
│   ├─┬ neon-animation#1.2.3
│   │ ├─┬ iron-meta#1.1.1
│   │ │ └── polymer#1.5.0
│   │ ├─┬ iron-resizable-behavior#1.0.3
│   │ │ └── polymer#1.5.0
│   │ ├─┬ iron-selector#1.5.2
│   │ │ └── polymer#1.5.0
│   │ ├── polymer#1.5.0
│   │ └── web-animations-js#2.2.1
│   ├─┬ paper-styles#1.1.4
│   │ ├── font-roboto#1.0.1
│   │ ├─┬ iron-flex-layout#1.3.1
│   │ │ └── polymer#1.5.0
│   │ └── polymer#1.5.0
│   └── polymer#1.5.0
├─┬ platinum-elements#2.0.0
│ ├─┬ platinum-bluetooth#2.1.0
│ │ ├── polymer#1.5.0
│ │ └─┬ promise-polyfill#1.0.0
│ │   └── polymer#1.5.0
│ ├─┬ platinum-https-redirect#1.0.2
│ │ └── polymer#1.5.0
│ ├─┬ platinum-push-messaging#1.0.5
│ │ ├── polymer#1.5.0
│ │ └─┬ promise-polyfill#1.0.0
│ │   └── polymer#1.5.0
│ └─┬ platinum-sw#1.3.0
│   ├── polymer#1.5.0
│   └── sw-toolbox#3.2.0
└─┬ polymer#1.5.0
  └── webcomponentsjs#0.7.22
```