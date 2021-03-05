# RoForums
A Roblox game to recreate the Roblox forums.

[Website](https://ethanmcbloxxer.github.io/RoForums/) • [Repository](https://github.com/EthanMcBloxxer/RoForums) • [Public Instance](https://roblox.com/games/5748548342/Forums-beta/) • [Official Group](https://roblox.com/groups/7833287/The-Forum-Recreators/) • [Discord](https://discord.gg/YsVWEhACsY)

![GitHub current release)](https://img.shields.io/github/v/release/EthanMcBloxxer/RoForums?include_prereleases&label=Current%20Version&style=for-the-badge) [![GitHub issues](https://img.shields.io/github/issues/EthanMcBloxxer/RoForums?style=for-the-badge)](https://github.com/EthanMcBloxxer/RoForums/issues) [![GitHub forks](https://img.shields.io/github/forks/EthanMcBloxxer/RoForums?style=for-the-badge)](https://github.com/EthanMcBloxxer/RoForums/network) [![GitHub stars](https://img.shields.io/github/stars/EthanMcBloxxer/RoForums?style=for-the-badge)](https://github.com/EthanMcBloxxer/RoForums/stargazers) [![GitHub license](https://img.shields.io/github/license/EthanMcBloxxer/RoForums?style=for-the-badge)](https://github.com/EthanMcBloxxer/RoForums/blob/main/license)

### Contributing
We can use every skill on this project. Whether you're a novice scripter or the most advanced mapmaker out there, we can probably use you on this project. If anything, I'm even looking for a new leader. So far, this is just a tiny project with barely any coverage. If you want to pitch in and help, we could use absolutely anything, as long as you know how to use Studio. Rojo support will come when Rojo allows storing instances, as I understand pull requests will become very difficult if multiple people have conflicting changes with the base file.  
Additionally, if you add any extra remote assets to RoForums, please list them in `assets.md`.

<details>
	<summary>Acceptable Syntax</summary>

* Always use tabs and proper indentation
* Don't include ending semicolons (;)
* Categorize scripts with markdown-inspired comments:
	* -- HEADING 1 -- (1-line padding at bottom if the next line is also a comment)
	* --- Heading 2 ---
	* ---- heading 3 ----
* Try to use absolute paths (like `game.Players.LocalPlayer` instead of `script.Parent.Parent`)
* Use `game.Workspace` instead of `workspace`
* Functionalize any multi-line code typed >5 times

</details>

If you want to, you can also [open an issue](https://github.com/EthanMcBloxxer/RoForums/issues/new?assignees=&labels=contributor+request&template=request--contributor--role.md&title=Contributor+request%3A+%5BYOUR-ROBLOX-USERNAME%5D) and request the contributor role, which allows you to upload assets to The Forums Recreators.

<!-- WAITING FOR ROJO MODEL SYNCING TO USE Also, the repository is initialized with Rojo. If you don't know how to use Rojo, we've bundled a Rojo v6.0.2 binary, so all you have to do when you clone the repository is open it in the console (command prompt) and execute `.\rojo serve .`, install the plugin, and connect. Then edit the scripts in your preferred editor, like Atom, Sublime, or VSC. When you're done, also do `.\rojo build -o roforums.rbxlx`. -->

### Mirroring
Since this code is open-source, you can easily make a seperate RoForums instance, kind of like you can with [Mastodon](https://joinmastodon.org).

### Implementing
If you are a developer and want to implement a RoForums instance inside of your game, then simply make a new place file and edit the categories, length, and DataStore parts of the script.

### License
The code here is licensed under the [MIT License](https://github.com/EthanMcBloxxer/RoForums/blob/main/license). This entails you must tell end users (players) that you are using code from here, simply and visibly. Copying snippets doesn't require immediate credit, but we would appriceate a mention in a "Credits" menu. Running your own instance of RoForums **requires** a visible and easy-to-read message with the shorturl of the project ([gh/EthanMcBloxxer/RoForums](https://github.com/EthanMcBloxxer/RoForums/)) or entire url ([github.com/EthanMcBloxxer/RoForums](https://github.com/EthanMcBloxxer/RoForums/)).

### Publications
If you'd like to drop a mention to this repository ([Tweet](https://twitter.com/intent/tweet?text=Wow:&url=https%3A%2F%2Fgithub.com%2FEthanMcBloxxer%2FRoForums)), then just request an edit to this file via editing or pull requesting and we'll review it. Please put it in the "Unofficial" section.
#### Official
[Recreating the Roblox Forums: Month 3](https://www.reddit.com/r/roblox/comments/jupx1w/recreating_the_roblox_forums_month_3/)  
["Recreating the Roblox Forums" Update](https://www.reddit.com/r/roblox/comments/lq3tuz/recreating_the_roblox_forums_update/)
#### Endorsed
[Roblox Forums Are Coming Back](https://www.youtube.com/watch?v=NJ7-1YtZol0)  
#### Unofficial
(none)  

<!--

// Storing the Rojo GitHub Action to automatically upload roforums.rbxlx to the Official Instance until Rojo is used

name: Deploy to Official Instance

on:
  push:
    branches:
      - main

jobs:
  ci:
    name: Deploy to Roblox
    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v1
      with:
        submodules: true

    - uses: Roblox/setup-foreman@v1
      with:
        version: "^1.0.0"
        token: ${{ secrets.GITHUB_TOKEN }}

    - name: Deploy
      run: rojo upload --cookie "$ROBLOSECURITY" --asset_id 5748548342
      env:
        ROBLOSECURITY: ${{ secrets.ROBLOSECURITY }}

-->
