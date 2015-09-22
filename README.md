# polymer-cdn <sub><sup>v1.1.3</sup></sub>
**A mirror of Polymer's components so that they can be used directly from CDN**

## How to use
In general, given an element named `my-cool-element`, the CDN url for it will be:
```
https://cdn.rawgit.com/download/polymer-cdn/1.1.3/lib/my-cool-element/my-cool-element.html
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
All these libraries can be found in the `lib` subfolder. These used to be links to the actual files, 
but it made updating painful so now I just copy the Bower output. You can browse the repo to locate
the files manually, or just trust Bower.

```sh
└── webcomponentsjs#0.7.12

paper-elements#1.0.5 lib\paper-elements
├── paper-badge#1.0.3
├── paper-behaviors#1.0.3
├── paper-button#1.0.6
├── paper-card#1.0.5
├── paper-checkbox#1.0.10
├── paper-dialog#1.0.1
├── paper-dialog-behavior#1.0.4
├── paper-dialog-scrollable#1.0.1
├── paper-drawer-panel#1.0.3
├── paper-dropdown-menu#1.0.2
├── paper-fab#1.0.4
├── paper-header-panel#1.0.5
├── paper-icon-button#1.0.3
├── paper-input#1.0.14
├── paper-item#1.0.2
├── paper-material#1.0.2
├── paper-menu#1.1.0
├── paper-menu-button#1.0.3
├── paper-progress#1.0.5
├── paper-radio-button#1.0.8
├── paper-radio-group#1.0.4
├── paper-ripple#1.0.2
├── paper-scroll-header-panel#1.0.8
├── paper-slider#1.0.6
├── paper-spinner#1.0.2
├── paper-styles#1.0.11
├── paper-tabs#1.0.2
├── paper-toast#1.0.0
├── paper-toggle-button#1.0.8
├── paper-toolbar#1.0.4
└── paper-tooltip#1.1.0

iron-autogrow-textarea#1.0.5 lib\iron-autogrow-textarea
├── iron-behaviors#1.0.8
├── iron-flex-layout#1.0.3
├── iron-form-element-behavior#1.0.4
├── iron-validatable-behavior#1.0.4
└── polymer#1.1.3

google-apis#1.1.0 lib\google-apis
├── iron-jsonp-library#1.0.3
└── polymer#1.1.3

iron-collapse#1.0.3 lib\iron-collapse
└── polymer#1.1.3

firebase-element#1.0.6 lib\firebase-element
├── firebase#2.2.9
└── polymer#1.1.3

google-map#1.1.0 lib\google-map
├── google-apis#1.1.0
├── iron-resizable-behavior#1.0.2
└── polymer#1.1.3

iron-behaviors#1.0.8 lib\iron-behaviors
├── iron-a11y-keys-behavior#1.0.5
└── polymer#1.1.3

google-analytics#1.2.0 lib\google-analytics
├── ga-api-utils#0.2.0
├── google-chart#1.0.2
├── google-signin#1.0.3
├── polymer#1.1.3
└── promise-polyfill#1.0.0

iron-flex-layout#1.0.3 lib\iron-flex-layout
└── polymer#1.1.3

iron-form-element-behavior#1.0.4 lib\iron-form-element-behavior
└── polymer#1.1.3

iron-dropdown#1.0.6 lib\iron-dropdown
├── iron-a11y-keys-behavior#1.0.5
├── iron-behaviors#1.0.8
├── iron-overlay-behavior#1.0.6
├── iron-resizable-behavior#1.0.2
├── neon-animation#1.0.6
└── polymer#1.1.3

iron-icon#1.0.4 lib\iron-icon
├── iron-flex-layout#1.0.3
├── iron-meta#1.0.3
└── polymer#1.1.3

iron-input#1.0.6 lib\iron-input
├── iron-validatable-behavior#1.0.4
└── polymer#1.1.3

iron-form#1.0.9 lib\iron-form
├── iron-ajax#1.0.4
└── polymer#1.1.3

iron-menu-behavior#1.0.3 lib\iron-menu-behavior
├── iron-a11y-keys-behavior#1.0.5
├── iron-selector#1.0.3
└── polymer#1.1.3

iron-overlay-behavior#1.0.6 lib\iron-overlay-behavior
├── iron-fit-behavior#1.0.3
├── iron-resizable-behavior#1.0.2
└── polymer#1.1.3

iron-test-helpers#1.0.3 lib\iron-test-helpers
└── polymer#1.1.3

iron-validatable-behavior#1.0.4 lib\iron-validatable-behavior
├── iron-meta#1.0.3
└── polymer#1.1.3

iron-doc-viewer#1.0.5 lib\iron-doc-viewer
├── marked-element#1.1.1
├── paper-button#1.0.6
├── paper-styles#1.0.11
├── polymer#1.1.3
└── prism-element#1.0.2

gold-cc-cvc-input#1.0.4 lib\gold-cc-cvc-input
├── iron-form-element-behavior#1.0.4
├── iron-icon#1.0.4
├── paper-input#1.0.14
├── paper-styles#1.0.11
└── polymer#1.1.3

marked-element#1.1.1 lib\marked-element
├── marked#0.3.5
└── polymer#1.1.3

iron-selector#1.0.3 lib\iron-selector
└── polymer#1.1.3

gold-phone-input#1.0.6 lib\gold-phone-input
├── iron-form-element-behavior#1.0.4
├── iron-input#1.0.6
├── paper-input#1.0.14
├── paper-styles#1.0.11
└── polymer#1.1.3

gold-zip-input#1.0.3 lib\gold-zip-input
├── iron-form-element-behavior#1.0.4
├── iron-icon#1.0.4
├── iron-validator-behavior#1.0.1
├── paper-input#1.0.14
├── paper-styles#1.0.11
└── polymer#1.1.3

gold-email-input#1.0.4 lib\gold-email-input
├── iron-form-element-behavior#1.0.4
├── iron-icon#1.0.4
├── paper-input#1.0.14
├── paper-styles#1.0.11
└── polymer#1.1.3

gold-cc-expiration-input#1.0.5 lib\gold-cc-expiration-input
├── iron-form-element-behavior#1.0.4
├── iron-validatable-behavior#1.0.4
├── iron-validator-behavior#1.0.1
├── paper-input#1.0.14
├── paper-styles#1.0.11
└── polymer#1.1.3

paper-material#1.0.2 lib\paper-material
├── paper-styles#1.0.11
└── polymer#1.1.3

platinum-push-messaging#1.0.3 lib\platinum-push-messaging
├── polymer#1.1.3
└── promise-polyfill#1.0.0

paper-ripple#1.0.2 lib\paper-ripple
├── iron-a11y-keys-behavior#1.0.5
└── polymer#1.1.3

gold-cc-input#1.0.6 lib\gold-cc-input
├── iron-form-element-behavior#1.0.4
├── iron-icon#1.0.4
├── iron-validator-behavior#1.0.1
├── paper-input#1.0.14
├── paper-styles#1.0.11
└── polymer#1.1.3

paper-header-panel#1.0.5 lib\paper-header-panel
├── iron-flex-layout#1.0.3
└── polymer#1.1.3

paper-dropdown-menu#1.0.2 lib\paper-dropdown-menu
├── iron-a11y-keys-behavior#1.0.5
├── iron-icon#1.0.4
├── iron-icons#1.0.3
├── paper-input#1.0.14
├── paper-menu-button#1.0.3
├── paper-ripple#1.0.2
├── paper-styles#1.0.11
└── polymer#1.1.3

paper-badge#1.0.3 lib\paper-badge
├── iron-resizable-behavior#1.0.2
├── paper-styles#1.0.11
└── polymer#1.1.3

paper-checkbox#1.0.10 lib\paper-checkbox
├── iron-checked-element-behavior#1.0.2
├── paper-behaviors#1.0.3
├── paper-ripple#1.0.2
├── paper-styles#1.0.11
└── polymer#1.1.3

paper-card#1.0.5 lib\paper-card
├── iron-flex-layout#1.0.3
├── paper-material#1.0.2
└── polymer#1.1.3

promise-polyfill#1.0.0 lib\promise-polyfill
└── polymer#1.1.3

paper-button#1.0.6 lib\paper-button
├── iron-flex-layout#1.0.3
├── paper-behaviors#1.0.3
├── paper-material#1.0.2
├── paper-ripple#1.0.2
└── polymer#1.1.3

iron-list#1.1.1 lib\iron-list
├── iron-resizable-behavior#1.0.2
└── polymer#1.1.3

paper-fab#1.0.4 lib\paper-fab
├── iron-flex-layout#1.0.3
├── iron-icon#1.0.4
├── iron-icons#1.0.3
├── paper-behaviors#1.0.3
├── paper-material#1.0.2
├── paper-ripple#1.0.2
├── paper-styles#1.0.11
└── polymer#1.1.3

paper-progress#1.0.5 lib\paper-progress
├── iron-range-behavior#1.0.2
├── paper-styles#1.0.11
└── polymer#1.1.3

paper-input#1.0.14 lib\paper-input
├── iron-autogrow-textarea#1.0.5
├── iron-behaviors#1.0.8
├── iron-form-element-behavior#1.0.4
├── iron-input#1.0.6
├── paper-styles#1.0.11
└── polymer#1.1.3

paper-menu-button#1.0.3 lib\paper-menu-button
├── iron-a11y-keys-behavior#1.0.5
├── iron-behaviors#1.0.8
├── iron-dropdown#1.0.6
├── neon-animation#1.0.6
├── paper-material#1.0.2
├── paper-styles#1.0.11
└── polymer#1.1.3

paper-menu#1.1.0 lib\paper-menu
├── iron-behaviors#1.0.8
├── iron-collapse#1.0.3
├── iron-menu-behavior#1.0.3
├── paper-styles#1.0.11
└── polymer#1.1.3

webcomponentsjs#0.7.12 lib\webcomponentsjs

paper-slider#1.0.6 lib\paper-slider
├── iron-a11y-keys-behavior#1.0.5
├── iron-behaviors#1.0.8
├── iron-flex-layout#1.0.3
├── iron-form-element-behavior#1.0.4
├── paper-behaviors#1.0.3
├── paper-input#1.0.14
├── paper-progress#1.0.5
├── paper-ripple#1.0.2
├── paper-styles#1.0.11
└── polymer#1.1.3

paper-toggle-button#1.0.8 lib\paper-toggle-button
├── iron-checked-element-behavior#1.0.2
├── paper-behaviors#1.0.3
├── paper-ripple#1.0.2
├── paper-styles#1.0.11
└── polymer#1.1.3

paper-radio-button#1.0.8 lib\paper-radio-button
├── iron-checked-element-behavior#1.0.2
├── paper-behaviors#1.0.3
├── paper-ripple#1.0.2
├── paper-styles#1.0.11
└── polymer#1.1.3

paper-tabs#1.0.2 lib\paper-tabs
├── iron-behaviors#1.0.8
├── iron-flex-layout#1.0.3
├── iron-icon#1.0.4
├── iron-iconset-svg#1.0.4
├── iron-menu-behavior#1.0.3
├── iron-resizable-behavior#1.0.2
├── paper-icon-button#1.0.3
├── paper-ripple#1.0.2
├── paper-styles#1.0.11
└── polymer#1.1.3

paper-tooltip#1.1.0 lib\paper-tooltip
├── neon-animation#1.0.6
├── paper-styles#1.0.11
└── polymer#1.1.3

hydrolysis#1.15.4 lib\hydrolysis

iron-checked-element-behavior#1.0.2 lib\iron-checked-element-behavior
├── iron-form-element-behavior#1.0.4
├── iron-validatable-behavior#1.0.4
└── polymer#1.1.3

paper-scroll-header-panel#1.0.8 lib\paper-scroll-header-panel
├── iron-resizable-behavior#1.0.2
├── paper-toolbar#1.0.4
└── polymer#1.1.3
```
