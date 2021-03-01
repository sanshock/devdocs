---
template: overrides/main.html
title: Getting started
---

# Getting started

netSys is a framework designed for modularity, simplicity, ease-of-use and compatibility.
It's simple to install netSys, use either [git][1] or [pack][3].

If you are experiencing problems, take a look at the [troubleshooting][2] section.

  [1]: #with-git
  [2]: troubleshooting.md
  [3]: #with-pack

## Installation

### with git

Installing netSys using `git` is the most common way to install netSys.

=== "git"

    ```
    git clone {URL}
    ```

### with pack

Installing netSys using `pack` is an alternative to git.

You can use `pack pickup` or `pack install`.


=== "pack install"

    ```
    pack install netsys
    ```

=== "pack pickup"

    ```
    pack pickup STAR_netsys
    ```


## Modules

By default, netSys is shipped with node.js and the following modules.

- @discordjs/opus
- @discordjs/discord.js
- @moldotla/dotenv
- @firebase/firebase-js-sdk
- fs
- @talmobi/yt-search
- @fent/node-ytdl-core

It is recommended to update these modules on a fresh install, you can use the terminal for this.


=== "npm"

    ```
    npm install 
    ```



