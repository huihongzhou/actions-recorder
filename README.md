
React Actions Recorder(like Redux)
----

Demo http://repo.tiye.me/actions-recorder/

Tricks:

* Click with "Shift" key pressing to step backward.
* set `inProduction` true if you want to limit size of `records` to `400`

### Usage

```bash
npm i --save actions-recorder
```

Get `recorder`:

```coffee
recorder = require 'actions-recorder'
```

Get Devtools:

```coffee
# for component
Devtools = require 'actions-recorder/lib/devtools'
```

`recorder` is a mutable object like store, with methods:

* `recorder.setup (options)`
* `recorder.request (store, recorder) ->`
* `recorder.getState ()`
* `recorder.getCore ()`
* `recorder.subscribe (store, recorder) ->`
* `recorder.ubsubscribe (listener)`
* `recorder.dispatch (actionType, actionData)`

`Devtools` is a component to show actions:

```coffee
React.createElement Devtools,
  records: Immutable.List()
  initial: Immutable.List()
  pointer: 0
  updater: (state, actionType, actionData) -> state
  isTravelling: false
  width: window.innerWidth
  height: window.innerHeight
```

Read code in `src/` to get more details.

### Background Image

http://www.fabuloussavers.com/new_wallpaper/DJ_Vinyl_Disc_freecomputerdesktopwallpaper_1920.jpg

### Development

https://github.com/mvc-works/webpack-workflow

### License

MIT
