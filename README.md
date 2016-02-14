# polymer-cdn <sup><sub>v1.2.4</sub></sup>
**A mirror of Polymer's components so that they can be used directly from CDN**

![Polymer CDN is powered by MaxCDN](http://i.imgur.com/9obTXpk.png)

## How to use
In general, given an element named `my-cool-element`, the CDN url for it will be:
```
https://cdn.rawgit.com/download/polymer-cdn/1.2.4/lib/my-cool-element/my-cool-element.html
```
To be sure, browse this repo and copy-paste the url to the raw version into [RawGit](https://rawgit.com).

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
All the libraries available in polymer-cdn can be found side-by-side in the [lib](https://github.com/Download/polymer-cdn/tree/1.2.4/lib) subfolder. 

Some of the libraries depend on other libraries. We call those other libraries the dependencies of the library.
These dependencies will also be pulled into your page when you include such a library. 
If the dependencies themselves depend on yet other libraries, these dependencies of dependencies will also be 
pulled into your page, et cetera until the full dependency tree has been loaded. We call this transitive 
dependency resolution and it's built in to the way Web Components work. 

The bower output below lists, for each library included in this CDN, the dependencies of that library. 
These dependencies are themselves also listed at the top-level, so you can work out the entire dependency
tree for a library by carefully examining this diagram.

```sh
polymer-cdn#1.2.4 C:\Users\Frank\Documents\GitHub\polymer-cdn
├─┬ gold-elements#1.0.1
│ ├─┬ gold-cc-cvc-input#1.0.6
│ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-icon#1.0.7
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├── paper-input#1.1.6
│ │ ├─┬ paper-styles#1.1.3
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ gold-cc-expiration-input#1.1.1
│ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-validatable-behavior#1.0.5
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-validator-behavior#1.0.1
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├── paper-input#1.1.6
│ │ ├─┬ paper-styles#1.1.3
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ gold-cc-input#1.0.7
│ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-icon#1.0.7
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-validator-behavior#1.0.1
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├── paper-input#1.1.6
│ │ ├─┬ paper-styles#1.1.3
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ gold-email-input#1.0.7
│ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-icon#1.0.7
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├── paper-input#1.1.6
│ │ ├─┬ paper-styles#1.1.3
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ gold-phone-input#1.0.7
│ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-input#1.0.8
│ │ │ ├─┬ iron-validatable-behavior#1.0.5
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├── paper-input#1.1.6
│ │ ├─┬ paper-styles#1.1.3
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ └─┬ gold-zip-input#1.0.5
│   ├─┬ iron-form-element-behavior#1.0.6
│   │ └── polymer#1.2.4
│   ├─┬ iron-icon#1.0.7
│   │ ├─┬ iron-flex-layout#1.2.3
│   │ │ └── polymer#1.2.4
│   │ ├─┬ iron-meta#1.1.1
│   │ │ └── polymer#1.2.4
│   │ └── polymer#1.2.4
│   ├─┬ iron-validator-behavior#1.0.1
│   │ ├─┬ iron-meta#1.1.1
│   │ │ └── polymer#1.2.4
│   │ └── polymer#1.2.4
│   ├── paper-input#1.1.6
│   ├─┬ paper-styles#1.1.3
│   │ ├── font-roboto#1.0.1
│   │ ├─┬ iron-flex-layout#1.2.3
│   │ │ └── polymer#1.2.4
│   │ └── polymer#1.2.4
│   └── polymer#1.2.4
├─┬ google-web-components#1.0.1
│ ├─┬ firebase-element#1.0.12
│ │ ├── firebase#2.4.0
│ │ └── polymer#1.2.4
│ ├─┬ google-analytics#1.2.1
│ │ ├── ga-api-utils#0.2.0 (latest is 0.4.0)
│ │ ├─┬ google-chart#1.0.4
│ │ │ ├─┬ google-apis#1.1.4
│ │ │ │ ├─┬ iron-jsonp-library#1.0.4
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-ajax#1.1.1
│ │ │ │ ├── polymer#1.2.4
│ │ │ │ └─┬ promise-polyfill#1.0.0
│ │ │ │   └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ google-signin#1.3.1
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ google-apis#1.1.4
│ │ │ │ ├─┬ iron-jsonp-library#1.0.4
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-icon#1.0.7
│ │ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ paper-material#1.0.6
│ │ │ │ ├─┬ paper-styles#1.1.3
│ │ │ │ │ ├── font-roboto#1.0.1
│ │ │ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ paper-ripple#1.0.5
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├── polymer#1.2.4
│ │ └─┬ promise-polyfill#1.0.0
│ │   └── polymer#1.2.4
│ ├─┬ google-apis#1.1.4
│ │ ├─┬ iron-jsonp-library#1.0.4
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ google-calendar#1.0.1
│ │ ├── google-apis#1.1.4
│ │ ├── google-signin#1.3.1
│ │ └── polymer#1.2.4
│ ├─┬ google-castable-video#1.0.2
│ │ └── polymer#1.2.4
│ ├─┬ google-chart#1.0.4
│ │ ├─┬ google-apis#1.1.4
│ │ │ ├─┬ iron-jsonp-library#1.0.4
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-ajax#1.1.1
│ │ │ ├── polymer#1.2.4
│ │ │ └─┬ promise-polyfill#1.0.0
│ │ │   └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ google-feeds#1.0.2
│ │ ├── google-apis#1.1.4
│ │ ├─┬ iron-jsonp-library#1.0.4
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ google-hangout-button#1.0.1
│ │ ├─┬ google-apis#1.1.4
│ │ │ ├─┬ iron-jsonp-library#1.0.4
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ google-map#1.1.10
│ │ ├── google-apis#1.1.4
│ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ └── polymer#1.2.4
│ │ ├── iron-selector#1.2.2
│ │ └── polymer#1.2.4
│ ├─┬ google-sheets#1.0.5
│ │ ├── google-apis#1.1.4
│ │ ├── google-signin#1.3.1
│ │ ├─┬ iron-ajax#1.1.1
│ │ │ ├── polymer#1.2.4
│ │ │ └─┬ promise-polyfill#1.0.0
│ │ │   └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ google-signin#1.3.1
│ │ ├── font-roboto#1.0.1
│ │ ├─┬ google-apis#1.1.4
│ │ │ ├─┬ iron-jsonp-library#1.0.4
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-icon#1.0.7
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-material#1.0.6
│ │ │ ├─┬ paper-styles#1.1.3
│ │ │ │ ├── font-roboto#1.0.1
│ │ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-ripple#1.0.5
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ google-streetview-pano#1.0.3
│ │ ├── google-apis#1.1.4
│ │ └── polymer#1.2.4
│ ├─┬ google-url-shortener#1.0.1
│ │ ├─┬ google-apis#1.1.4
│ │ │ ├─┬ iron-jsonp-library#1.0.4
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ google-youtube#1.2.0
│ │ ├─┬ google-apis#1.1.4
│ │ │ ├─┬ iron-jsonp-library#1.0.4
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-localstorage#1.0.5
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ └─┬ google-youtube-upload#1.1.2
│   ├── cors-upload-sample#37c97848a2
│   ├─┬ google-signin#1.3.1
│   │ ├── font-roboto#1.0.1
│   │ ├─┬ google-apis#1.1.4
│   │ │ ├─┬ iron-jsonp-library#1.0.4
│   │ │ │ └── polymer#1.2.4
│   │ │ └── polymer#1.2.4
│   │ ├─┬ iron-flex-layout#1.2.3
│   │ │ └── polymer#1.2.4
│   │ ├─┬ iron-icon#1.0.7
│   │ │ ├─┬ iron-flex-layout#1.2.3
│   │ │ │ └── polymer#1.2.4
│   │ │ ├─┬ iron-meta#1.1.1
│   │ │ │ └── polymer#1.2.4
│   │ │ └── polymer#1.2.4
│   │ ├─┬ paper-material#1.0.6
│   │ │ ├─┬ paper-styles#1.1.3
│   │ │ │ ├── font-roboto#1.0.1
│   │ │ │ ├─┬ iron-flex-layout#1.2.3
│   │ │ │ │ └── polymer#1.2.4
│   │ │ │ └── polymer#1.2.4
│   │ │ └── polymer#1.2.4
│   │ ├─┬ paper-ripple#1.0.5
│   │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│   │ │ │ └── polymer#1.2.4
│   │ │ └── polymer#1.2.4
│   │ └── polymer#1.2.4
│   └── polymer#1.2.4
├─┬ iron-elements#1.0.8
│ ├─┬ iron-a11y-announcer#1.0.4
│ │ └── polymer#1.2.4
│ ├─┬ iron-a11y-keys#1.0.4
│ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ └── polymer#1.2.4
│ ├─┬ iron-ajax#1.1.1
│ │ ├── polymer#1.2.4
│ │ └─┬ promise-polyfill#1.0.0
│ │   └── polymer#1.2.4
│ ├─┬ iron-autogrow-textarea#1.0.10
│ │ ├─┬ iron-behaviors#1.0.12
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-validatable-behavior#1.0.5
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ iron-behaviors#1.0.12
│ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ iron-checked-element-behavior#1.0.4
│ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-validatable-behavior#1.0.5
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ iron-collapse#1.0.6
│ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ iron-component-page#1.1.4
│ │ ├── hydrolysis#1.22.0
│ │ ├─┬ iron-ajax#1.1.1
│ │ │ ├── polymer#1.2.4
│ │ │ └─┬ promise-polyfill#1.0.0
│ │ │   └── polymer#1.2.4
│ │ ├─┬ iron-doc-viewer#1.0.12
│ │ │ ├─┬ marked-element#1.1.3
│ │ │ │ ├── marked#0.3.5
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ paper-button#1.0.11
│ │ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ paper-behaviors#1.0.11
│ │ │ │ │ ├─┬ iron-behaviors#1.0.12
│ │ │ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ ├─┬ iron-checked-element-behavior#1.0.4
│ │ │ │ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ │ ├─┬ iron-validatable-behavior#1.0.5
│ │ │ │ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ ├─┬ paper-ripple#1.0.5
│ │ │ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ paper-material#1.0.6
│ │ │ │ │ ├─┬ paper-styles#1.1.3
│ │ │ │ │ │ ├── font-roboto#1.0.1
│ │ │ │ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ paper-ripple#1.0.5
│ │ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ paper-styles#1.1.3
│ │ │ │ ├── font-roboto#1.0.1
│ │ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├── polymer#1.2.4
│ │ │ └─┬ prism-element#1.0.3
│ │ │   ├── polymer#1.2.4
│ │ │   └── prism#1.4.1
│ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-icons#1.1.3
│ │ │ ├─┬ iron-icon#1.0.7
│ │ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-iconset-svg#1.0.9
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-selector#1.2.2
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-header-panel#1.1.3
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-styles#1.1.3
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-toolbar#1.1.4
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ ├── paper-styles#1.1.3
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ iron-demo-helpers#1.1.0
│ │ ├─┬ iron-icons#1.1.3
│ │ │ ├─┬ iron-icon#1.0.7
│ │ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-iconset-svg#1.0.9
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ marked-element#1.1.3
│ │ │ ├── marked#0.3.5
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-icon-button#1.0.6
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-icon#1.0.7
│ │ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-icons#1.1.3
│ │ │ │ ├─┬ iron-icon#1.0.7
│ │ │ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ iron-iconset-svg#1.0.9
│ │ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ paper-behaviors#1.0.11
│ │ │ │ ├─┬ iron-behaviors#1.0.12
│ │ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ iron-checked-element-behavior#1.0.4
│ │ │ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ ├─┬ iron-validatable-behavior#1.0.5
│ │ │ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ paper-ripple#1.0.5
│ │ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ paper-ripple#1.0.5
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ paper-styles#1.1.3
│ │ │ │ ├── font-roboto#1.0.1
│ │ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-styles#1.1.3
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├── polymer#1.2.4
│ │ └── prism-element#1.0.3
│ ├── iron-doc-viewer#1.0.12
│ ├─┬ iron-dropdown#1.2.0
│ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-behaviors#1.0.12
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-overlay-behavior#1.3.1
│ │ │ ├─┬ iron-fit-behavior#1.0.5
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ └── polymer#1.2.4
│ │ ├─┬ neon-animation#1.1.0
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-selector#1.2.2
│ │ │ │ └── polymer#1.2.4
│ │ │ ├── polymer#1.2.4
│ │ │ └── web-animations-js#2.1.3 (latest is 2.1.4)
│ │ └── polymer#1.2.4
│ ├─┬ iron-fit-behavior#1.0.5
│ │ └── polymer#1.2.4
│ ├─┬ iron-flex-layout#1.2.3
│ │ └── polymer#1.2.4
│ ├─┬ iron-form#1.0.14
│ │ ├─┬ iron-ajax#1.1.1
│ │ │ ├── polymer#1.2.4
│ │ │ └─┬ promise-polyfill#1.0.0
│ │ │   └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ iron-form-element-behavior#1.0.6
│ │ └── polymer#1.2.4
│ ├─┬ iron-icon#1.0.7
│ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-meta#1.1.1
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ iron-icons#1.1.3
│ │ ├─┬ iron-icon#1.0.7
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-iconset-svg#1.0.9
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ iron-iconset#1.0.4
│ │ ├─┬ iron-meta#1.1.1
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ iron-iconset-svg#1.0.9
│ │ ├─┬ iron-meta#1.1.1
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├── iron-image#1.2.2
│ ├─┬ iron-input#1.0.8
│ │ ├─┬ iron-validatable-behavior#1.0.5
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ iron-jsonp-library#1.0.4
│ │ └── polymer#1.2.4
│ ├─┬ iron-label#1.0.2
│ │ └── polymer#1.2.4
│ ├─┬ iron-list#1.2.4
│ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-scroll-target-behavior#1.0.3
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ iron-localstorage#1.0.5
│ │ └── polymer#1.2.4
│ ├─┬ iron-media-query#1.0.8
│ │ └── polymer#1.2.4
│ ├─┬ iron-menu-behavior#1.1.1
│ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-selector#1.2.2
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ iron-meta#1.1.1
│ │ └── polymer#1.2.4
│ ├─┬ iron-overlay-behavior#1.3.1
│ │ ├─┬ iron-fit-behavior#1.0.5
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ iron-page-url#0.7.1
│ │ └── polymer#1.2.4
│ ├─┬ iron-pages#1.0.7
│ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-selector#1.2.2
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ iron-range-behavior#1.0.4
│ │ └── polymer#1.2.4
│ ├─┬ iron-resizable-behavior#1.0.3
│ │ └── polymer#1.2.4
│ ├─┬ iron-scroll-target-behavior#1.0.3
│ │ └── polymer#1.2.4
│ ├─┬ iron-scroll-threshold#1.0.1
│ │ ├─┬ iron-scroll-target-behavior#1.0.3
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ iron-selector#1.2.2
│ │ └── polymer#1.2.4
│ ├─┬ iron-signals#1.0.3
│ │ └── polymer#1.2.4
│ ├─┬ iron-swipeable-container#1.0.2
│ │ └── polymer#1.2.4
│ ├─┬ iron-test-helpers#1.1.3
│ │ └── polymer#1.2.4
│ ├─┬ iron-validatable-behavior#1.0.5
│ │ ├─┬ iron-meta#1.1.1
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ └─┬ iron-validator-behavior#1.0.1
│   ├─┬ iron-meta#1.1.1
│   │ └── polymer#1.2.4
│   └── polymer#1.2.4
├─┬ molecules#1.0.0
│ └─┬ marked-element#1.1.3
│   ├── marked#0.3.5
│   └── polymer#1.2.4
├─┬ neon-elements#1.0.0
│ └─┬ neon-animation#1.1.0
│   ├─┬ iron-meta#1.1.1
│   │ └── polymer#1.2.4
│   ├─┬ iron-resizable-behavior#1.0.3
│   │ └── polymer#1.2.4
│   ├─┬ iron-selector#1.2.2
│   │ └── polymer#1.2.4
│   ├── polymer#1.2.4
│   └── web-animations-js#2.1.3
├─┬ paper-elements#1.0.7
│ ├─┬ paper-badge#1.1.1
│ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-styles#1.1.3
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ paper-behaviors#1.0.11
│ │ ├─┬ iron-behaviors#1.0.12
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-checked-element-behavior#1.0.4
│ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-validatable-behavior#1.0.5
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-ripple#1.0.5
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ paper-button#1.0.11
│ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-behaviors#1.0.11
│ │ │ ├─┬ iron-behaviors#1.0.12
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-checked-element-behavior#1.0.4
│ │ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ iron-validatable-behavior#1.0.5
│ │ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ paper-ripple#1.0.5
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-material#1.0.6
│ │ │ ├─┬ paper-styles#1.1.3
│ │ │ │ ├── font-roboto#1.0.1
│ │ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-ripple#1.0.5
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ paper-card#1.1.1
│ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-image#1.2.2
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-material#1.0.6
│ │ │ ├─┬ paper-styles#1.1.3
│ │ │ │ ├── font-roboto#1.0.1
│ │ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├── paper-styles#1.1.3
│ │ └── polymer#1.2.4
│ ├─┬ paper-checkbox#1.1.2
│ │ ├─┬ iron-checked-element-behavior#1.0.4
│ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-validatable-behavior#1.0.5
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-behaviors#1.0.11
│ │ │ ├─┬ iron-behaviors#1.0.12
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-checked-element-behavior#1.0.4
│ │ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ iron-validatable-behavior#1.0.5
│ │ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ paper-ripple#1.0.5
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-ripple#1.0.5
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├── paper-styles#1.1.3
│ │ └── polymer#1.2.4
│ ├─┬ paper-dialog#1.0.4
│ │ ├─┬ neon-animation#1.1.0
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-selector#1.2.2
│ │ │ │ └── polymer#1.2.4
│ │ │ ├── polymer#1.2.4
│ │ │ └── web-animations-js#2.1.3
│ │ ├─┬ paper-dialog-behavior#1.2.0
│ │ │ ├─┬ iron-overlay-behavior#1.3.1
│ │ │ │ ├─┬ iron-fit-behavior#1.0.5
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├── paper-styles#1.1.3
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-styles#1.1.3
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ paper-dialog-behavior#1.2.0
│ │ ├─┬ iron-overlay-behavior#1.3.1
│ │ │ ├─┬ iron-fit-behavior#1.0.5
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├── paper-styles#1.1.3
│ │ └── polymer#1.2.4
│ ├─┬ paper-dialog-scrollable#1.1.1
│ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-styles#1.1.3
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ paper-drawer-panel#1.0.6
│ │ ├─┬ iron-media-query#1.0.8
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-selector#1.2.2
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ paper-dropdown-menu#1.1.3
│ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-icon#1.0.7
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-icons#1.1.3
│ │ │ ├─┬ iron-icon#1.0.7
│ │ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-iconset-svg#1.0.9
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-validatable-behavior#1.0.5
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-input#1.1.6
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-autogrow-textarea#1.0.10
│ │ │ │ ├─┬ iron-behaviors#1.0.12
│ │ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ iron-validatable-behavior#1.0.5
│ │ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-behaviors#1.0.12
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-input#1.0.8
│ │ │ │ ├─┬ iron-validatable-behavior#1.0.5
│ │ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├── paper-styles#1.1.3
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-menu-button#1.0.4
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-behaviors#1.0.12
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-dropdown#1.2.0
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ iron-behaviors#1.0.12
│ │ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ iron-overlay-behavior#1.3.1
│ │ │ │ │ ├─┬ iron-fit-behavior#1.0.5
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ neon-animation#1.1.0
│ │ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ ├─┬ iron-selector#1.2.2
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ ├── polymer#1.2.4
│ │ │ │ │ └── web-animations-js#2.1.3
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ neon-animation#1.1.0
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ iron-selector#1.2.2
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├── polymer#1.2.4
│ │ │ │ └── web-animations-js#2.1.3
│ │ │ ├─┬ paper-material#1.0.6
│ │ │ │ ├─┬ paper-styles#1.1.3
│ │ │ │ │ ├── font-roboto#1.0.1
│ │ │ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ paper-styles#1.1.3
│ │ │ │ ├── font-roboto#1.0.1
│ │ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-ripple#1.0.5
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-styles#1.1.3
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ paper-fab#1.2.0
│ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-icon#1.0.7
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-icons#1.1.3
│ │ │ ├─┬ iron-icon#1.0.7
│ │ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-iconset-svg#1.0.9
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-behaviors#1.0.11
│ │ │ ├─┬ iron-behaviors#1.0.12
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-checked-element-behavior#1.0.4
│ │ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ iron-validatable-behavior#1.0.5
│ │ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ paper-ripple#1.0.5
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├── paper-material#1.0.6
│ │ ├─┬ paper-styles#1.1.3
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ paper-header-panel#1.1.3
│ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ paper-icon-button#1.0.6
│ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-icon#1.0.7
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-icons#1.1.3
│ │ │ ├─┬ iron-icon#1.0.7
│ │ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-iconset-svg#1.0.9
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-behaviors#1.0.11
│ │ │ ├─┬ iron-behaviors#1.0.12
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-checked-element-behavior#1.0.4
│ │ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ iron-validatable-behavior#1.0.5
│ │ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ paper-ripple#1.0.5
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-ripple#1.0.5
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-styles#1.1.3
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├── paper-input#1.1.6
│ ├─┬ paper-item#1.1.3
│ │ ├─┬ iron-behaviors#1.0.12
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-styles#1.1.3
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ paper-listbox#1.1.2
│ │ ├─┬ iron-behaviors#1.0.12
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-collapse#1.0.6
│ │ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-menu-behavior#1.1.1
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-selector#1.2.2
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-styles#1.1.3
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ paper-material#1.0.6
│ │ ├─┬ paper-styles#1.1.3
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ paper-menu#1.2.2
│ │ ├─┬ iron-behaviors#1.0.12
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-collapse#1.0.6
│ │ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-menu-behavior#1.1.1
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-selector#1.2.2
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-styles#1.1.3
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ paper-menu-button#1.0.4
│ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-behaviors#1.0.12
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-dropdown#1.2.0
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-behaviors#1.0.12
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-overlay-behavior#1.3.1
│ │ │ │ ├─┬ iron-fit-behavior#1.0.5
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ neon-animation#1.1.0
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ iron-selector#1.2.2
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├── polymer#1.2.4
│ │ │ │ └── web-animations-js#2.1.3
│ │ │ └── polymer#1.2.4
│ │ ├─┬ neon-animation#1.1.0
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-selector#1.2.2
│ │ │ │ └── polymer#1.2.4
│ │ │ ├── polymer#1.2.4
│ │ │ └── web-animations-js#2.1.3
│ │ ├─┬ paper-material#1.0.6
│ │ │ ├─┬ paper-styles#1.1.3
│ │ │ │ ├── font-roboto#1.0.1
│ │ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-styles#1.1.3
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ paper-progress#1.0.8
│ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-range-behavior#1.0.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-styles#1.1.3
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ paper-radio-button#1.0.12
│ │ ├─┬ iron-checked-element-behavior#1.0.4
│ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-validatable-behavior#1.0.5
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-behaviors#1.0.11
│ │ │ ├─┬ iron-behaviors#1.0.12
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-checked-element-behavior#1.0.4
│ │ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ iron-validatable-behavior#1.0.5
│ │ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ paper-ripple#1.0.5
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-ripple#1.0.5
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-styles#1.1.3
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ paper-radio-group#1.0.9
│ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-selector#1.2.2
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ paper-ripple#1.0.5
│ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ paper-scroll-header-panel#1.0.15
│ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ paper-slider#1.0.9
│ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-behaviors#1.0.12
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-behaviors#1.0.11
│ │ │ ├─┬ iron-behaviors#1.0.12
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-checked-element-behavior#1.0.4
│ │ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ iron-validatable-behavior#1.0.5
│ │ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ paper-ripple#1.0.5
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├── paper-input#1.1.6
│ │ ├─┬ paper-progress#1.0.8
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-range-behavior#1.0.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ paper-styles#1.1.3
│ │ │ │ ├── font-roboto#1.0.1
│ │ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-styles#1.1.3
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ paper-spinner#1.1.0
│ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-styles#1.1.3
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ paper-styles#1.1.3
│ │ ├── font-roboto#1.0.1
│ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ paper-tabs#1.3.5
│ │ ├─┬ iron-behaviors#1.0.12
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-icon#1.0.7
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ iron-iconset-svg#1.0.9
│ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├── iron-menu-behavior#1.1.1
│ │ ├─┬ iron-resizable-behavior#1.0.3
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-behaviors#1.0.11
│ │ │ ├─┬ iron-behaviors#1.0.12
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-checked-element-behavior#1.0.4
│ │ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ iron-validatable-behavior#1.0.5
│ │ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ paper-ripple#1.0.5
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-icon-button#1.0.6
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-icon#1.0.7
│ │ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-icons#1.1.3
│ │ │ │ ├─┬ iron-icon#1.0.7
│ │ │ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ iron-iconset-svg#1.0.9
│ │ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ paper-behaviors#1.0.11
│ │ │ │ ├─┬ iron-behaviors#1.0.12
│ │ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ iron-checked-element-behavior#1.0.4
│ │ │ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ ├─┬ iron-validatable-behavior#1.0.5
│ │ │ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ paper-ripple#1.0.5
│ │ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ paper-ripple#1.0.5
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ paper-styles#1.1.3
│ │ │ │ ├── font-roboto#1.0.1
│ │ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-styles#1.1.3
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ paper-toast#1.1.3
│ │ ├─┬ iron-a11y-announcer#1.0.4
│ │ │ └── polymer#1.2.4
│ │ ├── iron-overlay-behavior#1.3.1
│ │ ├─┬ paper-styles#1.1.3
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ paper-toggle-button#1.0.14
│ │ ├─┬ iron-checked-element-behavior#1.0.4
│ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-validatable-behavior#1.0.5
│ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-behaviors#1.0.11
│ │ │ ├─┬ iron-behaviors#1.0.12
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ iron-checked-element-behavior#1.0.4
│ │ │ │ ├─┬ iron-form-element-behavior#1.0.6
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ ├─┬ iron-validatable-behavior#1.0.5
│ │ │ │ │ ├─┬ iron-meta#1.1.1
│ │ │ │ │ │ └── polymer#1.2.4
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ ├─┬ paper-ripple#1.0.5
│ │ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ │ └── polymer#1.2.4
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-ripple#1.0.5
│ │ │ ├─┬ iron-a11y-keys-behavior#1.1.1
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ ├─┬ paper-styles#1.1.3
│ │ │ ├── font-roboto#1.0.1
│ │ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ │ └── polymer#1.2.4
│ │ │ └── polymer#1.2.4
│ │ └── polymer#1.2.4
│ ├─┬ paper-toolbar#1.1.4
│ │ ├─┬ iron-flex-layout#1.2.3
│ │ │ └── polymer#1.2.4
│ │ ├── paper-styles#1.1.3
│ │ └── polymer#1.2.4
│ └─┬ paper-tooltip#1.1.1
│   ├─┬ neon-animation#1.1.0
│   │ ├─┬ iron-meta#1.1.1
│   │ │ └── polymer#1.2.4
│   │ ├─┬ iron-resizable-behavior#1.0.3
│   │ │ └── polymer#1.2.4
│   │ ├─┬ iron-selector#1.2.2
│   │ │ └── polymer#1.2.4
│   │ ├── polymer#1.2.4
│   │ └── web-animations-js#2.1.3
│   ├─┬ paper-styles#1.1.3
│   │ ├── font-roboto#1.0.1
│   │ ├─┬ iron-flex-layout#1.2.3
│   │ │ └── polymer#1.2.4
│   │ └── polymer#1.2.4
│   └── polymer#1.2.4
├─┬ platinum-elements#2.0.0
│ ├─┬ platinum-bluetooth#2.0.0
│ │ ├── polymer#1.2.4
│ │ └─┬ promise-polyfill#1.0.0
│ │   └── polymer#1.2.4
│ ├─┬ platinum-https-redirect#1.0.1
│ │ └── polymer#1.2.4
│ ├─┬ platinum-push-messaging#1.0.5
│ │ ├── polymer#1.2.4
│ │ └─┬ promise-polyfill#1.0.0
│ │   └── polymer#1.2.4
│ └─┬ platinum-sw#1.2.3
│   ├── polymer#1.2.4
│   └── sw-toolbox#2.1.0 (latest is 3.1.1)
└─┬ polymer#1.2.4
  └── webcomponentsjs#0.7.20
```