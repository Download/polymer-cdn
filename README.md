# polymer-cdn <sup><sub>v1.2.3</sub></sup>
**A mirror of Polymer's components so that they can be used directly from CDN**

![Polymer CDN is powered by MaxCDN](http://i.imgur.com/9obTXpk.png)

## How to use
In general, given an element named `my-cool-element`, the CDN url for it will be:
```
https://cdn.rawgit.com/download/polymer-cdn/1.2.3/lib/my-cool-element/my-cool-element.html
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
All the libraries available in polymer-cdn can be found side-by-side in the [lib](https://github.com/Download/polymer-cdn/tree/1.2.3/lib) subfolder. 

Some of the libraries depend on other libraries. We call those other libraries the dependencies of the library.
These dependencies will also be pulled into your page when you include such a library. 
If the dependencies themselves depend on yet other libraries, these dependencies of dependencies will also be 
pulled into your page, et cetera until the full dependency tree has been loaded. We call this transitive 
dependency resolution and it's built in to the way Web Components work. 

The bower output below lists, for each library included in this CDN, the dependencies of that library. 
These dependencies are themselves also listed at the top-level, so you can work out the entire dependency
tree for a library by carefully examining this diagram.

```sh
polymer#1.2.3 lib\polymer
└── webcomponentsjs#0.7.18

paper-elements#1.0.6 lib\paper-elements
├── paper-badge#1.0.4
├── paper-behaviors#1.0.10
├── paper-button#1.0.8
├── paper-card#1.0.8
├── paper-checkbox#1.0.15
├── paper-dialog#1.0.3
├── paper-dialog-behavior#1.1.0
├── paper-dialog-scrollable#1.1.0
├── paper-drawer-panel#1.0.5
├── paper-dropdown-menu#1.1.0
├── paper-fab#1.1.0
├── paper-header-panel#1.1.1
├── paper-icon-button#1.0.5
├── paper-input#1.1.1
├── paper-item#1.1.2
├── paper-listbox#1.0.0
├── paper-material#1.0.4
├── paper-menu#1.2.0
├── paper-menu-button#1.0.3
├── paper-progress#1.0.7
├── paper-radio-button#1.0.11
├── paper-radio-group#1.0.6
├── paper-ripple#1.0.5
├── paper-scroll-header-panel#1.0.12
├── paper-slider#1.0.8
├── paper-spinner#1.0.4
├── paper-styles#1.0.13
├── paper-tabs#1.1.0
├── paper-toast#1.1.0
├── paper-toggle-button#1.0.11
├── paper-toolbar#1.1.1
└── paper-tooltip#1.1.1

iron-dropdown#1.0.6 lib\iron-dropdown
├── iron-a11y-keys-behavior#1.1.0
├── iron-behaviors#1.0.11
├── iron-overlay-behavior#1.0.9
├── iron-resizable-behavior#1.0.2
├── neon-animation#1.0.8
└── polymer#1.2.3

gold-cc-expiration-input#1.1.0 lib\gold-cc-expiration-input
├── iron-flex-layout#1.2.1
├── iron-form-element-behavior#1.0.5
├── iron-validatable-behavior#1.0.5
├── iron-validator-behavior#1.0.1
├── paper-input#1.1.1
├── paper-styles#1.0.13
└── polymer#1.2.3

iron-a11y-announcer#1.0.4 lib\iron-a11y-announcer
└── polymer#1.2.3

gold-phone-input#1.0.7 lib\gold-phone-input
├── iron-flex-layout#1.2.1
├── iron-form-element-behavior#1.0.5
├── iron-input#1.0.7
├── paper-input#1.1.1
├── paper-styles#1.0.13
└── polymer#1.2.3

gold-email-input#1.0.6 lib\gold-email-input
├── iron-form-element-behavior#1.0.5
├── iron-icon#1.0.7
├── paper-input#1.1.1
├── paper-styles#1.0.13
└── polymer#1.2.3

gold-cc-cvc-input#1.0.5 lib\gold-cc-cvc-input
├── iron-flex-layout#1.2.1
├── iron-form-element-behavior#1.0.5
├── iron-icon#1.0.7
├── paper-input#1.1.1
├── paper-styles#1.0.13
└── polymer#1.2.3

gold-zip-input#1.0.4 lib\gold-zip-input
├── iron-form-element-behavior#1.0.5
├── iron-icon#1.0.7
├── iron-validator-behavior#1.0.1
├── paper-input#1.1.1
├── paper-styles#1.0.13
└── polymer#1.2.3

iron-autogrow-textarea#1.0.10 lib\iron-autogrow-textarea
├── iron-behaviors#1.0.11
├── iron-flex-layout#1.2.1
├── iron-form-element-behavior#1.0.5
├── iron-validatable-behavior#1.0.5
└── polymer#1.2.3

iron-a11y-keys-behavior#1.1.0 lib\iron-a11y-keys-behavior
└── polymer#1.2.3

iron-a11y-keys#1.0.4 lib\iron-a11y-keys
├── iron-a11y-keys-behavior#1.1.0
└── polymer#1.2.3

iron-ajax#1.1.1 lib\iron-ajax
├── polymer#1.2.3
└── promise-polyfill#1.0.0

gold-cc-input#1.0.7 lib\gold-cc-input
├── iron-flex-layout#1.2.1
├── iron-form-element-behavior#1.0.5
├── iron-icon#1.0.7
├── iron-validator-behavior#1.0.1
├── paper-input#1.1.1
├── paper-styles#1.0.13
└── polymer#1.2.3

iron-collapse#1.0.4 lib\iron-collapse
└── polymer#1.2.3

iron-form-element-behavior#1.0.5 lib\iron-form-element-behavior
└── polymer#1.2.3

iron-checked-element-behavior#1.0.3 lib\iron-checked-element-behavior
├── iron-form-element-behavior#1.0.5
├── iron-validatable-behavior#1.0.5
└── polymer#1.2.3

iron-fit-behavior#1.0.5 lib\iron-fit-behavior
└── polymer#1.2.3

iron-behaviors#1.0.11 lib\iron-behaviors
├── iron-a11y-keys-behavior#1.1.0
└── polymer#1.2.3

iron-flex-layout#1.2.1 lib\iron-flex-layout
└── polymer#1.2.3

iron-component-page#1.1.1 lib\iron-component-page
├── hydrolysis#1.21.4
├── iron-ajax#1.1.1
├── iron-doc-viewer#1.0.10
├── iron-flex-layout#1.2.1
├── iron-icons#1.0.5
├── iron-selector#1.0.8
├── paper-header-panel#1.1.1
├── paper-styles#1.0.13
├── paper-toolbar#1.1.1
└── polymer#1.2.3

iron-form#1.0.13 lib\iron-form
├── iron-ajax#1.1.1
└── polymer#1.2.3

iron-icon#1.0.7 lib\iron-icon
├── iron-flex-layout#1.2.1
├── iron-meta#1.1.1
└── polymer#1.2.3

iron-iconset-svg#1.0.9 lib\iron-iconset-svg
├── iron-meta#1.1.1
└── polymer#1.2.3

iron-image#1.0.4 lib\iron-image
├── iron-flex-layout#1.2.1
└── polymer#1.2.3

iron-iconset#1.0.4 lib\iron-iconset
├── iron-meta#1.1.1
└── polymer#1.2.3

iron-input#1.0.7 lib\iron-input
├── iron-validatable-behavior#1.0.5
└── polymer#1.2.3

iron-meta#1.1.1 lib\iron-meta
└── polymer#1.2.3

iron-localstorage#1.0.5 lib\iron-localstorage
└── polymer#1.2.3

iron-jsonp-library#1.0.4 lib\iron-jsonp-library
└── polymer#1.2.3

iron-doc-viewer#1.0.10 lib\iron-doc-viewer
├── marked-element#1.1.1
├── paper-button#1.0.8
├── paper-styles#1.0.13
├── polymer#1.2.3
└── prism-element#1.0.3

iron-media-query#1.0.7 lib\iron-media-query
└── polymer#1.2.3

iron-range-behavior#1.0.4 lib\iron-range-behavior
└── polymer#1.2.3

iron-pages#1.0.4 lib\iron-pages
├── iron-resizable-behavior#1.0.2
├── iron-selector#1.0.8
└── polymer#1.2.3

iron-signals#1.0.3 lib\iron-signals
└── polymer#1.2.3

neon-animation#1.0.8 lib\neon-animation
├── iron-meta#1.1.1
├── iron-resizable-behavior#1.0.2
├── iron-selector#1.0.8
├── paper-styles#1.0.13
├── polymer#1.2.3
└── web-animations-js#2.1.2

iron-menu-behavior#1.0.6 lib\iron-menu-behavior
├── iron-a11y-keys-behavior#1.1.0
├── iron-selector#1.0.8
└── polymer#1.2.3

iron-validatable-behavior#1.0.5 lib\iron-validatable-behavior
├── iron-meta#1.1.1
└── polymer#1.2.3

google-feeds#1.0.2 lib\google-feeds
├── google-apis#1.1.3
├── iron-jsonp-library#1.0.4
└── polymer#1.2.3

iron-icons#1.0.5 lib\iron-icons
├── iron-icon#1.0.7
├── iron-iconset-svg#1.0.9
└── polymer#1.2.3

iron-selector#1.0.8 lib\iron-selector
└── polymer#1.2.3

iron-overlay-behavior#1.0.9 lib\iron-overlay-behavior
├── iron-fit-behavior#1.0.5
├── iron-resizable-behavior#1.0.2
└── polymer#1.2.3

google-signin#1.2.0 lib\google-signin
├── font-roboto#1.0.1
├── google-apis#1.1.3
├── iron-flex-layout#1.2.1
├── iron-icon#1.0.7
├── iron-icons#1.0.5
├── paper-material#1.0.4
├── paper-ripple#1.0.5
└── polymer#1.2.3

iron-test-helpers#1.1.0 lib\iron-test-helpers
└── polymer#1.2.3

google-sheets#1.0.5 lib\google-sheets
├── google-apis#1.1.3
├── google-signin#1.2.0
├── iron-ajax#1.1.1
└── polymer#1.2.3

google-analytics#1.2.1 lib\google-analytics
├── ga-api-utils#0.2.0
├── google-chart#1.0.4
├── google-signin#1.2.0
├── polymer#1.2.3
└── promise-polyfill#1.0.0

google-castable-video#1.0.2 lib\google-castable-video
└── polymer#1.2.3

google-chart#1.0.4 lib\google-chart
├── google-apis#1.1.3
├── iron-ajax#1.1.1
└── polymer#1.2.3

iron-list#1.1.6 lib\iron-list
├── iron-resizable-behavior#1.0.2
└── polymer#1.2.3

firebase-element#1.0.8 lib\firebase-element
├── firebase#2.3.2
└── polymer#1.2.3

google-apis#1.1.3 lib\google-apis
├── iron-jsonp-library#1.0.4
└── polymer#1.2.3

platinum-push-messaging#1.0.5 lib\platinum-push-messaging
├── polymer#1.2.3
└── promise-polyfill#1.0.0

paper-listbox#1.0.0 lib\paper-listbox
├── iron-behaviors#1.0.11
├── iron-collapse#1.0.4
├── iron-menu-behavior#1.0.6
├── paper-styles#1.0.13
└── polymer#1.2.3

google-map#1.1.7 lib\google-map
├── google-apis#1.1.3
├── iron-resizable-behavior#1.0.2
├── iron-selector#1.0.8
└── polymer#1.2.3

paper-badge#1.0.4 lib\paper-badge
├── iron-resizable-behavior#1.0.2
├── paper-styles#1.0.13
└── polymer#1.2.3

paper-behaviors#1.0.10 lib\paper-behaviors
├── iron-behaviors#1.0.11
├── iron-checked-element-behavior#1.0.3
└── polymer#1.2.3

paper-button#1.0.8 lib\paper-button
├── iron-flex-layout#1.2.1
├── paper-behaviors#1.0.10
├── paper-material#1.0.4
├── paper-ripple#1.0.5
└── polymer#1.2.3

paper-checkbox#1.0.15 lib\paper-checkbox
├── iron-checked-element-behavior#1.0.3
├── paper-behaviors#1.0.10
├── paper-ripple#1.0.5
├── paper-styles#1.0.13
└── polymer#1.2.3

paper-dialog#1.0.3 lib\paper-dialog
├── neon-animation#1.0.8
├── paper-dialog-behavior#1.1.0
├── paper-styles#1.0.13
└── polymer#1.2.3

paper-dialog-scrollable#1.1.0 lib\paper-dialog-scrollable
└── polymer#1.2.3

paper-dialog-behavior#1.1.0 lib\paper-dialog-behavior
├── iron-overlay-behavior#1.0.9
├── paper-styles#1.0.13
└── polymer#1.2.3

paper-drawer-panel#1.0.5 lib\paper-drawer-panel
├── iron-media-query#1.0.7
├── iron-resizable-behavior#1.0.2
├── iron-selector#1.0.8
└── polymer#1.2.3

paper-item#1.1.2 lib\paper-item
├── iron-behaviors#1.0.11
├── iron-flex-layout#1.2.1
├── paper-styles#1.0.13
└── polymer#1.2.3

promise-polyfill#1.0.0 lib\promise-polyfill
└── polymer#1.2.3

paper-icon-button#1.0.5 lib\paper-icon-button
├── iron-flex-layout#1.2.1
├── iron-icon#1.0.7
├── iron-icons#1.0.5
├── paper-behaviors#1.0.10
├── paper-ripple#1.0.5
├── paper-styles#1.0.13
└── polymer#1.2.3

paper-dropdown-menu#1.1.0 lib\paper-dropdown-menu
├── iron-a11y-keys-behavior#1.1.0
├── iron-form-element-behavior#1.0.5
├── iron-icon#1.0.7
├── iron-icons#1.0.5
├── iron-validatable-behavior#1.0.5
├── paper-input#1.1.1
├── paper-menu-button#1.0.3
├── paper-ripple#1.0.5
├── paper-styles#1.0.13
└── polymer#1.2.3

paper-material#1.0.4 lib\paper-material
├── paper-styles#1.0.13
└── polymer#1.2.3

paper-card#1.0.8 lib\paper-card
├── iron-flex-layout#1.2.1
├── iron-image#1.0.4
├── paper-material#1.0.4
└── polymer#1.2.3

paper-radio-button#1.0.11 lib\paper-radio-button
├── iron-checked-element-behavior#1.0.3
├── paper-behaviors#1.0.10
├── paper-ripple#1.0.5
├── paper-styles#1.0.13
└── polymer#1.2.3

paper-header-panel#1.1.1 lib\paper-header-panel
├── iron-flex-layout#1.2.1
└── polymer#1.2.3

webcomponentsjs#0.7.18 lib\webcomponentsjs

paper-radio-group#1.0.6 lib\paper-radio-group
├── iron-a11y-keys-behavior#1.1.0
├── iron-selector#1.0.8
└── polymer#1.2.3

paper-spinner#1.0.4 lib\paper-spinner
├── iron-flex-layout#1.2.1
├── paper-styles#1.0.13
└── polymer#1.2.3

font-roboto#1.0.1 lib\font-roboto

paper-ripple#1.0.5 lib\paper-ripple
├── iron-a11y-keys-behavior#1.1.0
└── polymer#1.2.3

paper-tooltip#1.1.1 lib\paper-tooltip
├── neon-animation#1.0.8
├── paper-styles#1.0.13
└── polymer#1.2.3

paper-menu#1.2.0 lib\paper-menu
├── iron-behaviors#1.0.11
├── iron-collapse#1.0.4
├── iron-flex-layout#1.2.1
├── iron-menu-behavior#1.0.6
├── paper-styles#1.0.13
└── polymer#1.2.3

paper-toast#1.1.0 lib\paper-toast
├── iron-a11y-announcer#1.0.4
├── iron-overlay-behavior#1.0.9
├── paper-styles#1.0.13
└── polymer#1.2.3

paper-tabs#1.1.0 lib\paper-tabs
├── iron-behaviors#1.0.11
├── iron-flex-layout#1.2.1
├── iron-icon#1.0.7
├── iron-iconset-svg#1.0.9
├── iron-menu-behavior#1.0.6
├── iron-resizable-behavior#1.0.2
├── paper-behaviors#1.0.10
├── paper-icon-button#1.0.5
├── paper-styles#1.0.13
└── polymer#1.2.3

paper-toggle-button#1.0.11 lib\paper-toggle-button
├── iron-checked-element-behavior#1.0.3
├── paper-behaviors#1.0.10
├── paper-ripple#1.0.5
├── paper-styles#1.0.13
└── polymer#1.2.3

paper-scroll-header-panel#1.0.12 lib\paper-scroll-header-panel
├── iron-resizable-behavior#1.0.2
└── polymer#1.2.3

paper-toolbar#1.1.1 lib\paper-toolbar
├── iron-flex-layout#1.2.1
├── paper-styles#1.0.13
└── polymer#1.2.3

paper-slider#1.0.8 lib\paper-slider
├── iron-a11y-keys-behavior#1.1.0
├── iron-behaviors#1.0.11
├── iron-flex-layout#1.2.1
├── iron-form-element-behavior#1.0.5
├── paper-behaviors#1.0.10
├── paper-input#1.1.1
├── paper-progress#1.0.7
├── paper-ripple#1.0.5
├── paper-styles#1.0.13
└── polymer#1.2.3

cors-upload-sample#37c97848a2 lib\cors-upload-sample

paper-input#1.1.1 lib\paper-input
├── iron-autogrow-textarea#1.0.10
├── iron-behaviors#1.0.11
├── iron-form-element-behavior#1.0.5
├── iron-input#1.0.7
├── paper-styles#1.0.13
└── polymer#1.2.3

paper-fab#1.1.0 lib\paper-fab
├── iron-flex-layout#1.2.1
├── iron-icon#1.0.7
├── iron-icons#1.0.5
├── paper-behaviors#1.0.10
├── paper-material#1.0.4
├── paper-ripple#1.0.5
├── paper-styles#1.0.13
└── polymer#1.2.3

paper-styles#1.0.13 lib\paper-styles
├── font-roboto#1.0.1
├── iron-flex-layout#1.2.1
└── polymer#1.2.3

prism-element#1.0.3 lib\prism-element
├── polymer#1.2.3
└── prism#1.3.0

hydrolysis#1.21.4 lib\hydrolysis

firebase#2.3.2 lib\firebase

prism#1.3.0 lib\prism
```
