# Contributing to the development of Polymer CDN

If Polymer had a new release that you want to try and it's not here yet
on Polymer CDN, you can help yourself and contribute to this project.
Follow these steps to make a new version of Polymer available on Polymer CDN.

## Prerequisites
Before you start, make sure you have installed [Node JS](https://nodejs.org/en/),
[NPM](https://www.npmjs.com/) (comes with Node) and [Bower](https://bower.io/).
Haven't used Node JS yet? See this as an excuse to try the water. You'll love it!
As far as Git itself goes, I assume you already have it, but I can recommend
installing the [TortoiseGit](https://tortoisegit.org/) client. It's great and
it's what I'm using in this guide.

## Fork this project
This is recommended even if you just use `polymer-cdn`, because it gives you full
control over the contents of the CDN and is so easy to do. Just press that button
on the top right and hit it!

![Fork polymer-cdn](https://cdn.rawgit.com/Download/polymer-cdn/1.6.0/doc/fork.png)

## Clone your fork
Clone your fork to your local machine.

![Clone your fork](https://cdn.rawgit.com/Download/polymer-cdn/1.6.0/doc/clone.png)

## Create a branch and switch to it
This is a very important step as it will make it much easier later on to create a
Pull Request. Don't forget this step!

![Create a branch](https://cdn.rawgit.com/Download/polymer-cdn/1.6.0/doc/branch.png)

*(If you are like me and already started editing before realizing you need a new branch,
the easiest thing to do in my experience is to Stash Save your changes. Git will store
your changes out of sight and restore your workspace. You can then create the branch
and Stash Pop your changes on top of that. Make sure you include untracked changes)*

## Edit bower.json

**This step is optional.** Normally all versions will be set to #latest so you only have
to run `bower update` (next step), but sometimes (like for me today as I'm writing
this) you want to upgrade to a specific version of Polymer or one of the components.
In that case, just list that version in `bower.json` beforehand.

```json
{
  ..

  "dependencies": {
    "polymer": "Polymer/polymer#1.6.0",
    "paper-elements": "polymerelements/paper-elements#latest",
    "iron-elements": "polymerelements/iron-elements#latest",
    "neon-elements": "polymerelements/neon-elements#latest",
    "gold-elements": "polymerelements/gold-elements#latest",
    "platinum-elements": "polymerelements/platinum-elements#latest",
    "app-elements": "polymerelements/app-elements#0.9.0",
    "google-web-components": "GoogleWebComponents/google-web-components#latest",
    "molecules": "polymerelements/molecules#latest"
  }
}
```

## Run bower update
Open a command prompt in the root of the `polymer-cdn` project and run `bower update`.

```sh
$ bower update
```

## Copy the dependency tree to README.md
In the root of the project, run
```sh
bower list
````
Copy the resulting dependency tree and paste it at the bottom of `README.md`

## Add your name to the contributors section in package.json
Just copy-paste one of the existing contributor sections and fill in your info.

## Bump the version
Change the version number in a few places. It should match the Polymer version,
unless there is a second release with the same Polymer version, in which case
we append a `.2`, or a `.3` for the third release etc. For example: `1.4.0.2`

Use search/replace to change the old version to the new one in these files:
* package.json
* bower.json
* README.md

## Commit your changes
Commit your changes with a commit message that describes what changed.

## Push them to GitHub
Like the title says :)

## Test them with rawgit
You can test it by opening this [Codepen](http://codepen.io/StijnDeWitt/pen/EyPyyL)
and replacing the url in the `<base href="..">` tag at the top with one that points
to the new branch on your fork.

## Create a Pull Request
After you've tested (and possibly committed and pushed fixes), you can create a
Pull Request (PR). If you go to your fork on GitHub, you'll notice a bar at the
top of the screen with a nice and shiny green button:

![Pull request](https://cdn.rawgit.com/Download/polymer-cdn/1.6.0/doc/pr.png)

I can't wait until you click that one!


