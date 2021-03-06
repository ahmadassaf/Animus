<div style="text-align:center"><img src="https://github.com/dasilvacontin/animus/raw/master/screenshots/demo.png" width="1191"></div>

# animus

[![travis][travis-image]][travis-url]
[![js-standard-style][standard-image]][standard-url]

[travis-image]: https://travis-ci.org/dasilvacontin/animus.svg?style=flat
[travis-url]: https://travis-ci.org/dasilvacontin/animus
[standard-image]: https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat
[standard-url]: https://github.com/feross/standard

Chrome Extension for instantly storing and filtering your ideas, todos, links, check-laters.

[Install][animus-chrome-web-store] the Chrome Extension, and help us make it better! After installing the extension, you should be able to open *animus* over 'any' website using the toggle command (Ctrl+Shift+A by default).

*Content scripts can't modify some websites/paths, like the Chrome Web Store, any `chrome://...` window, your homepage, the new tab window, ... so you won't be able to open animus there, for now.*

*Also, you can't use animus on tabs that were open before installing the extension... Known bug.*

## Features

- **Hashtags and URLs** are parsed from the entries' text
- Fully usable via **keyboard shortcuts**
- **Filter** entries by text and hashtags
- **Storage sync** with your Google Account
- **Quickly opens** using a single command

## Keyboard Shortcuts

- <kbd>ctrl</kbd> + <kbd>shift</kbd> + <kbd>A</kbd> - Default command for toggling animus (open/close)
- <kbd>alt</kbd> + <kbd>shift</kbd> + <kbd>A</kbd> - Open animus and add the website's title and url to the input field
- <kbd>J</kbd> - Select next entry
- <kbd>K</kbd> - Select previous entry
- <kbd>tab</kbd> - Switch focus between the input field and the list
- <kbd>A</kbd>, add - Switch focus to input field
- <kbd>enter</kbd> - Insert input field's text as a new entry
- <kbd>shift</kbd> + <kbd>enter</kbd> - Same as above but it also closes animus
- <kbd>E</kbd>, edit - Edits the selected entry
- <kbd>D</kbd>, delete/done - Deletes the selected entry
- <kbd>U</kbd>, undo - Undoes the previous action
- <kbd>F</kbd>, follow link - Opens the selected entry's link in a new tab
- <kbd>esc</kbd> - Close animus

You can change/set a custom command for toggling animus in the **Keyboard shortcuts** configuration modal at the bottom of the [Chrome Extensions](chrome://extensions/) page.

## Roadmap

- Reminders via natural language processing
- GitHub integrations, eg repo/issue/PR status in entries with a GH link
- Progress bars for entries
- Translucent background
- Tests, specially those related to editing the database
- Make it fully usable without the need of key shortcuts

## Dev

```bash
$ npm install
$ gulp watch
```

Running `gulp` will generate a build of the extension at `dist/`. Running
`gulp watch` (recommended) will watch for changes in the source code and
automatically rebuild the project for you.

Here's how you install the dev build of the extension:

* navigate to `chrome://extensions`
* activate the `Developer Mode` using the checkbox at the top-right
* click the `Load unpacked extension...` button and select the `dist/` folder

**NB** you must manually reload the unpacked extension at `chrome://extensions`
_every time_ you make changes to it. This is very cumbersome, so I'd recommend
using this [Extension Reloader](https://chrome.google.com/webstore/detail/extensions-reloader/fimgfedafeadlieiabdeeaodndnlbhid).

## License

MIT. Copyright (c) [David da Silva Contin](http://dasilvacont.in).

<img src="https://github.com/dasilvacontin/animus/raw/master/app/img/logo384.png" width="192">

[animus-chrome-web-store]: https://chrome.google.com/webstore/detail/animus/hhlengghgfcjkfkfaocfnimlhnkjddch
