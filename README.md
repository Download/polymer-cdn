# polymer-cdn <sup><sub>v2.6.0.2</sub></sup>
**A mirror of Polymer's components so that they can be used directly from CDN**

![Polymer CDN is powered by MaxCDN](http://i.imgur.com/9obTXpk.png)

```
❗  Polymer CDN now supports Polymer 2! Please report any issues you may find.
```

## How to use
In general, given an element named `my-cool-element`, the CDN url for it will be:
```
https://cdn.rawgit.com/download/polymer-cdn/2.6.0.2/lib/my-cool-element/my-cool-element.html
```
To be sure, browse this repo and copy-paste the url to the raw version into [RawGit](https://rawgit.com).

## Try a pen
Try hacking on this [Codepen](https://codepen.io/StijnDeWitt/pen/XEejLe).

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
All the libraries available in polymer-cdn can be found side-by-side in the [lib](https://github.com/Download/polymer-cdn/tree/2.6.0/lib) subfolder. Contained therein are all elements [listed as compatible with Polymer 2](https://www.polymer-project.org/2.0/docs/about_20#elements).

> It looks like `gold-zip-input` wasn't actually ported to Polymer 2 yet at the time of writing this, despite being listed as compatible, as witnessed by incompatibility warnings concerning this element in the Bower output at the bottom of this page. Your mileage with this element may vary.

Some of the libraries depend on other libraries. We call those other libraries the dependencies of the library.
These dependencies will also be pulled into your page when you include such a library.
If the dependencies themselves depend on yet other libraries, these dependencies of dependencies will also be
pulled into your page, et cetera until the full dependency tree has been loaded. We call this transitive
dependency resolution and it's built in to the way Web Components work.

The bower output below lists, for each library included in this CDN, the dependencies of that library.
These dependencies are themselves also listed at the top-level, so you can work out the entire dependency
tree for a library by carefully examining this diagram.

```sh
polymer-cdn#2.6.0.2
├─┬ app-layout#2.1.0
│ ├─┬ iron-flex-layout#2.0.3
│ │ └─┬ polymer#2.6.0
│ │   ├── shadycss#1.1.2
│ │   └── webcomponentsjs#1.1.1
│ ├─┬ iron-media-query#2.1.0
│ │ └── polymer#2.6.0
│ ├─┬ iron-resizable-behavior#2.1.0
│ │ └── polymer#2.6.0
│ ├─┬ iron-scroll-target-behavior#2.1.0
│ │ └── polymer#2.6.0
│ └── polymer#2.6.0
├─┬ app-localize-behavior#2.0.1
│ ├── intl-messageformat#1.3.0 (latest is 2.2.0)
│ ├─┬ iron-ajax#2.1.3
│ │ └── polymer#2.6.0
│ └── polymer#2.6.0
├─┬ app-pouchdb#2.1.1
│ ├─┬ app-storage#2.1.1
│ │ └── polymer#2.6.0
│ ├── polymer#2.6.0
│ ├── pouchdb#6.4.3
│ └── pouchdb-find#0.10.5
├─┬ app-route#2.1.0
│ ├─┬ iron-location#2.2.0
│ │ └── polymer#2.6.0
│ └── polymer#2.6.0
├── app-storage#2.1.1
├─┬ gold-zip-input#2.1.0
│ ├─┬ iron-form-element-behavior#2.1.1
│ │ └── polymer#2.6.0
│ ├─┬ iron-icon#2.1.0
│ │ ├── iron-flex-layout#2.0.3
│ │ ├─┬ iron-meta#2.1.0
│ │ │ └── polymer#2.6.0
│ │ └── polymer#2.6.0
│ ├─┬ iron-validator-behavior#2.1.0
│ │ ├── iron-meta#2.1.0
│ │ └── polymer#2.6.0
│ ├─┬ paper-input#2.2.0
│ │ ├── iron-a11y-keys-behavior#2.1.0
│ │ ├─┬ iron-autogrow-textarea#2.2.0
│ │ │ ├─┬ iron-behaviors#2.1.1
│ │ │ │ ├─┬ iron-a11y-keys-behavior#2.1.0
│ │ │ │ │ └── polymer#2.6.0
│ │ │ │ └── polymer#2.6.0
│ │ │ ├── iron-flex-layout#2.0.3
│ │ │ ├─┬ iron-validatable-behavior#2.1.0
│ │ │ │ ├── iron-meta#2.1.0
│ │ │ │ └── polymer#2.6.0
│ │ │ └── polymer#2.6.0
│ │ ├── iron-behaviors#2.1.1
│ │ ├── iron-form-element-behavior#2.1.1
│ │ ├─┬ iron-input#2.1.2
│ │ │ ├─┬ iron-a11y-announcer#2.1.0
│ │ │ │ └── polymer#2.6.0
│ │ │ ├── iron-validatable-behavior#2.1.0
│ │ │ └── polymer#2.6.0
│ │ ├─┬ paper-styles#2.1.0
│ │ │ ├── font-roboto#1.1.0
│ │ │ ├── iron-flex-layout#2.0.3
│ │ │ └── polymer#2.6.0
│ │ └── polymer#2.6.0
│ ├── paper-styles#2.1.0
│ └── polymer#2.6.0
├── iron-a11y-announcer#2.1.0
├─┬ iron-a11y-keys#2.1.1
│ ├── iron-a11y-keys-behavior#2.1.0
│ └── polymer#2.6.0
├── iron-a11y-keys-behavior#2.1.0
├── iron-ajax#2.1.3
├── iron-autogrow-textarea#2.2.0
├── iron-behaviors#2.1.1
├─┬ iron-checked-element-behavior#2.1.0
│ ├── iron-form-element-behavior#2.1.1
│ ├── iron-validatable-behavior#2.1.0
│ └── polymer#2.6.0
├─┬ iron-collapse#2.2.0
│ ├── iron-resizable-behavior#2.1.0
│ └── polymer#2.6.0
├─┬ iron-component-page#3.0.1
│ ├── app-layout#2.1.0
│ ├── iron-ajax#2.1.3
│ ├─┬ iron-doc-viewer#3.2.0
│ │ ├── iron-location#2.2.0
│ │ ├─┬ marked-element#2.4.0
│ │ │ ├── marked#0.3.18 (0.3.19 available)
│ │ │ └── polymer#2.6.0
│ │ ├── paper-styles#2.1.0
│ │ ├── polymer#2.6.0
│ │ └─┬ prism-element#2.1.0
│ │   ├── polymer#2.6.0
│ │   └── prism#1.13.0
│ ├─┬ iron-icons#2.1.1
│ │ ├── iron-icon#2.1.0
│ │ ├─┬ iron-iconset-svg#2.2.0
│ │ │ ├── iron-meta#2.1.0
│ │ │ └── polymer#2.6.0
│ │ └── polymer#2.6.0
│ ├─┬ paper-icon-button#2.2.0
│ │ ├── iron-icon#2.1.0
│ │ ├─┬ paper-behaviors#2.1.0
│ │ │ ├── iron-behaviors#2.1.1
│ │ │ ├── iron-checked-element-behavior#2.1.0
│ │ │ ├─┬ paper-ripple#2.1.0
│ │ │ │ ├── iron-a11y-keys-behavior#2.1.0
│ │ │ │ └── polymer#2.6.0
│ │ │ └── polymer#2.6.0
│ │ ├── paper-styles#2.1.0
│ │ └── polymer#2.6.0
│ ├── paper-styles#2.1.0
│ ├─┬ paper-toast#2.1.0
│ │ ├── iron-a11y-announcer#2.1.0
│ │ ├── iron-fit-behavior#2.1.1
│ │ ├─┬ iron-overlay-behavior#2.3.3
│ │ │ ├── iron-a11y-keys-behavior#2.1.0
│ │ │ ├─┬ iron-fit-behavior#2.1.1
│ │ │ │ └── polymer#2.6.0
│ │ │ ├── iron-resizable-behavior#2.1.0
│ │ │ └── polymer#2.6.0
│ │ └── polymer#2.6.0
│ └── polymer#2.6.0
├─┬ iron-demo-helpers#2.1.0
│ ├── font-roboto#1.1.0
│ ├── iron-flex-layout#2.0.3
│ ├── iron-location#2.2.0
│ ├── marked-element#2.4.0
│ ├── polymer#2.6.0
│ └── prism-element#2.1.0
├── iron-doc-viewer#3.2.0
├─┬ iron-dropdown#2.2.0
│ ├── iron-behaviors#2.1.1
│ ├── iron-overlay-behavior#2.3.3
│ ├─┬ neon-animation#2.2.1
│ │ ├── iron-resizable-behavior#2.1.0
│ │ ├─┬ iron-selector#2.1.0
│ │ │ └── polymer#2.6.0
│ │ └── polymer#2.6.0
│ └── polymer#2.6.0
├── iron-fit-behavior#2.1.1
├── iron-flex-layout#2.0.3
├─┬ iron-form#2.2.1
│ ├── iron-ajax#2.1.3
│ └── polymer#2.6.0
├── iron-form-element-behavior#2.1.1
├── iron-icon#2.1.0
├── iron-icons#2.1.1
├─┬ iron-iconset#2.1.0
│ ├── iron-meta#2.1.0
│ └── polymer#2.6.0
├── iron-iconset-svg#2.2.0
├─┬ iron-image#2.2.0
│ └── polymer#2.6.0
├── iron-input#2.1.2
├─┬ iron-jsonp-library#2.1.0
│ └── polymer#2.6.0
├─┬ iron-label#2.1.0
│ └── polymer#2.6.0
├─┬ iron-list#2.0.13
│ ├── iron-a11y-keys-behavior#2.1.0
│ ├── iron-resizable-behavior#2.1.0
│ ├── iron-scroll-target-behavior#2.1.0
│ └── polymer#2.6.0
├─┬ iron-localstorage#2.1.1
│ └── polymer#2.6.0
├── iron-location#2.2.0
├── iron-media-query#2.1.0
├─┬ iron-menu-behavior#2.1.0
│ ├── iron-a11y-keys-behavior#2.1.0
│ ├── iron-flex-layout#2.0.3
│ ├── iron-selector#2.1.0
│ └── polymer#2.6.0
├── iron-meta#2.1.0
├── iron-overlay-behavior#2.3.3
├─┬ iron-pages#2.1.0
│ ├── iron-resizable-behavior#2.1.0
│ ├── iron-selector#2.1.0
│ └── polymer#2.6.0
├─┬ iron-range-behavior#2.1.0
│ └── polymer#2.6.0
├── iron-resizable-behavior#2.1.0
├── iron-scroll-target-behavior#2.1.0
├─┬ iron-scroll-threshold#2.0.0
│ ├── iron-scroll-target-behavior#2.1.0
│ └── polymer#2.6.0
├── iron-selector#2.1.0
├─┬ iron-test-helpers#2.0.0
│ └── polymer#2.6.0
├── iron-validatable-behavior#2.1.0
├── iron-validator-behavior#2.1.0
├── marked-element#2.4.0
├── neon-animation#2.2.1
├─┬ note-app-elements#2.1.2
│ ├── app-storage#2.1.1
│ ├── font-roboto#1.1.0
│ ├── iron-autogrow-textarea#2.2.0
│ ├── iron-flex-layout#2.0.3
│ ├── iron-icon#2.1.0
│ ├── iron-icons#2.1.1
│ ├── iron-input#2.1.2
│ ├─┬ paper-button#2.1.0
│ │ ├── iron-flex-layout#2.0.3
│ │ ├── paper-behaviors#2.1.0
│ │ ├── paper-styles#2.1.0
│ │ └── polymer#2.6.0
│ ├─┬ paper-fab#2.1.0
│ │ ├── iron-flex-layout#2.0.3
│ │ ├── iron-icon#2.1.0
│ │ ├── paper-behaviors#2.1.0
│ │ ├── paper-styles#2.1.0
│ │ └── polymer#2.6.0
│ ├── paper-icon-button#2.2.0
│ ├── paper-styles#2.1.0
│ ├── polymer#2.6.0
│ └── web-animations-js#2.3.1
├─┬ paper-alert-dialog#2.0.1
│ ├── iron-icon#2.1.0
│ ├── paper-button#2.1.0
│ ├─┬ paper-dialog#2.1.1
│ │ ├── iron-overlay-behavior#2.3.3
│ │ ├── neon-animation#2.2.1
│ │ ├─┬ paper-dialog-behavior#2.2.0
│ │ │ ├── iron-overlay-behavior#2.3.3
│ │ │ ├── paper-styles#2.1.0
│ │ │ └── polymer#2.6.0
│ │ └── polymer#2.6.0
│ └── polymer#2.6.0
├─┬ paper-badge#2.1.0
│ ├── iron-flex-layout#2.0.3
│ ├── iron-icon#2.1.0
│ ├── iron-resizable-behavior#2.1.0
│ ├── paper-styles#2.1.0
│ └── polymer#2.6.0
├── paper-behaviors#2.1.0
├── paper-button#2.1.0
├─┬ paper-card#2.1.0
│ ├── iron-flex-layout#2.0.3
│ ├── iron-image#2.2.0
│ ├── paper-styles#2.1.0
│ └── polymer#2.6.0
├─┬ paper-checkbox#2.0.2
│ ├── iron-a11y-keys-behavior#2.1.0
│ ├── iron-checked-element-behavior#2.1.0
│ ├── paper-behaviors#2.1.0
│ ├── paper-ripple#2.1.0
│ ├── paper-styles#2.1.0
│ └── polymer#2.6.0
├─┬ paper-dialog#2.1.1
│ ├── iron-overlay-behavior#2.3.3
│ ├── neon-animation#2.2.1
│ ├─┬ paper-dialog-behavior#2.2.0
│ │ ├── iron-overlay-behavior#2.3.3
│ │ ├── paper-styles#2.1.0
│ │ └── polymer#2.6.0
│ └── polymer#2.6.0
├── paper-dialog-behavior#2.2.0
├─┬ paper-dialog-scrollable#2.2.0
│ ├── iron-flex-layout#2.0.3
│ ├── paper-dialog-behavior#2.2.0
│ ├── paper-styles#2.1.0
│ └── polymer#2.6.0
├─┬ paper-drawer-panel#2.1.1
│ ├── iron-media-query#2.1.0
│ ├── iron-resizable-behavior#2.1.0
│ ├── iron-selector#2.1.0
│ └── polymer#2.6.0
├─┬ paper-dropdown-menu#2.1.0
│ ├── iron-a11y-keys-behavior#2.1.0
│ ├── iron-form-element-behavior#2.1.1
│ ├── iron-icon#2.1.0
│ ├── iron-iconset-svg#2.2.0
│ ├── iron-validatable-behavior#2.1.0
│ ├── paper-behaviors#2.1.0
│ ├── paper-input#2.2.0
│ ├─┬ paper-menu-button#2.1.0
│ │ ├── iron-a11y-keys-behavior#2.1.0
│ │ ├── iron-behaviors#2.1.1
│ │ ├── iron-dropdown#2.2.0
│ │ ├── iron-fit-behavior#2.1.1
│ │ ├── neon-animation#2.2.1
│ │ ├── paper-styles#2.1.0
│ │ └── polymer#2.6.0
│ ├── paper-ripple#2.1.0
│ ├── paper-styles#2.1.0
│ └── polymer#2.6.0
├── paper-fab#2.1.0
├─┬ paper-header-panel#2.1.0
│ ├── iron-flex-layout#2.0.3
│ └── polymer#2.6.0
├── paper-icon-button#2.2.0
├── paper-input#2.2.0
├─┬ paper-item#2.1.0
│ ├── iron-behaviors#2.1.1
│ ├── iron-flex-layout#2.0.3
│ ├── paper-styles#2.1.0
│ └── polymer#2.6.0
├─┬ paper-listbox#2.1.0
│ ├── iron-behaviors#2.1.1
│ ├── iron-menu-behavior#2.1.0
│ ├── paper-styles#2.1.0
│ └── polymer#2.6.0
├─┬ paper-material#2.1.0
│ ├── paper-styles#2.1.0
│ └── polymer#2.6.0
├── paper-menu-button#2.1.0
├─┬ paper-progress#2.1.0
│ ├── iron-flex-layout#2.0.3
│ ├── iron-range-behavior#2.1.0
│ ├── paper-styles#2.1.0
│ └── polymer#2.6.0
├─┬ paper-radio-button#2.1.0
│ ├── iron-checked-element-behavior#2.1.0
│ ├── iron-flex-layout#2.0.3
│ ├── paper-behaviors#2.1.0
│ ├── paper-styles#2.1.0
│ └── polymer#2.6.0
├─┬ paper-radio-group#2.2.0
│ ├── iron-a11y-keys-behavior#2.1.0
│ ├── iron-menu-behavior#2.1.0
│ ├── paper-radio-button#2.1.0
│ └── polymer#2.6.0
├── paper-ripple#2.1.0
├─┬ paper-scroll-header-panel#2.0.0
│ ├── iron-resizable-behavior#2.1.0
│ └── polymer#2.6.0
├─┬ paper-slider#2.0.5
│ ├── iron-a11y-keys-behavior#2.1.0
│ ├── iron-behaviors#2.1.1
│ ├── iron-flex-layout#2.0.3
│ ├── iron-form-element-behavior#2.1.1
│ ├── paper-behaviors#2.1.0
│ ├── paper-input#2.2.0
│ ├── paper-progress#2.1.0
│ ├── paper-styles#2.1.0
│ └── polymer#2.6.0
├─┬ paper-spinner#2.1.0
│ ├── paper-styles#2.1.0
│ └── polymer#2.6.0
├── paper-styles#2.1.0
├─┬ paper-swatch-picker#2.2.0
│ ├── iron-flex-layout#2.0.3
│ ├── iron-iconset-svg#2.2.0
│ ├── paper-icon-button#2.2.0
│ ├── paper-item#2.1.0
│ ├── paper-listbox#2.1.0
│ ├── paper-menu-button#2.1.0
│ └── polymer#2.6.0
├─┬ paper-tabs#2.1.0
│ ├── iron-behaviors#2.1.1
│ ├── iron-flex-layout#2.0.3
│ ├── iron-icon#2.1.0
│ ├── iron-iconset-svg#2.2.0
│ ├── iron-menu-behavior#2.1.0
│ ├── iron-resizable-behavior#2.1.0
│ ├── paper-behaviors#2.1.0
│ ├── paper-icon-button#2.2.0
│ ├── paper-styles#2.1.0
│ └── polymer#2.6.0
├── paper-toast#2.1.0
├─┬ paper-toggle-button#2.1.0
│ ├── iron-checked-element-behavior#2.1.0
│ ├── paper-behaviors#2.1.0
│ ├── paper-styles#2.1.0
│ └── polymer#2.6.0
├─┬ paper-toolbar#2.1.0
│ ├── iron-flex-layout#2.0.3
│ ├── paper-styles#2.1.0
│ └── polymer#2.6.0
├─┬ paper-tooltip#2.1.1
│ ├── paper-styles#2.1.0
│ └── polymer#2.6.0
├─┬ platinum-sw#2.1.0
│ ├── polymer#2.6.0
│ └── sw-toolbox#3.6.1
├── polymer#2.6.0
├─┬ polymerfire#2.2.1
│ ├── app-storage#2.1.1
│ ├── firebase#4.12.0
│ └── polymer#2.6.0
├── prism-element#2.1.0
├─┬ web-component-tester#6.5.0 (6.6.0-pre.3 available)
│ ├── accessibility-developer-tools#2.12.0
│ ├── async#1.5.2 (latest is 2.6.0)
│ ├── chai#3.5.0 (latest is 4.1.2)
│ ├── lodash#3.10.1 (3.11.0-npm-packages available, latest is 4.17.8-es)
│ ├── mocha#3.5.3 (latest is 5.0.5)
│ ├── sinon-chai#2.14.0 (latest is 3.0.0)
│ ├── sinonjs#1.17.1
│ ├── stacky#1.3.2
│ └── test-fixture#3.0.0
└── webcomponentsjs#1.1.1
```
