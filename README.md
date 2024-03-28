A pywal and [wallust](https://codeberg.org/explosion-mental/wallust) template for [Vencord](https://github.com/Vendicated/Vencord) (or probably any other client capable of loading css, no guarantees).

Does not modify any discord styling outside of colors - it is just a recolored, vanilla discord.

Is uses the same formula for generating background color shades as [Pywalfox](https://github.com/Frewacom/pywalfox/tree/master), so the colors will match :)

Dark theme only, sorry, I don't really use light themes, though it might work ok with `pywal -l`. If you edit the template because you use light themes with wal - feel free to PR!

## Usage

### pywal
Add the `discord-pywal.css` file to your `$HOME\.config\wal\templates`. After generating a pallette with `wal` there will be a `discord-pywal.css` file in your `$HOME\.cache\wal` directory.
See [https://github.com/dylanaraps/pywal/wiki/User-Template-Files](https://github.com/dylanaraps/pywal/wiki/User-Template-Files) for more information

You can then copy the cached theme to `$HOME\AppData\Roaming\Vencord\themes\pywal.css` in the script you run to update things after running wal or w/e. Then you can enable it in the Vencord settings.

### wallust
When using wallust you first need to check which version you have. You can do that by running this command:
```sh
wallust --version
```

<details>
<summary>Should your version be >= than 3.0.0 follow this guide</summary>

Copy `discord-wallust-beta.css` to `%appdata%\wallust` and
add this line to your `%appdata%\wallust\wallust.toml`

```toml
vencord = { template = 'discord-wallust-beta.css', target = 'C:/Users/Username/AppData/Roaming/Vencord/themes/wallust.css' }
```

Note that for toml, that *has* to be on one line. As an alternative, you can also write:

```toml
[templates]
[templates.vencord]
template = 'discord-wallust.css'
target = 'C:/Users/Gremious/AppData/Roaming/Vencord/themes/wallust.css'
```
</details>

<details>
<summary>Otherwise please follow these instructions</summary>

Copy `discord-wallust.css` to `%appdata%\wallust` and
add this to your `%appdata%\wallust\wallust.toml`

```toml
[[entry]]
template = 'discord-wallust.css'
target = 'C:/Users/Username/AppData/Roaming/Vencord/themes/wallust.css'
```
</details>

## Editing
I have left a bunch of notes and commented styles, and the color variable names are pretty self-explanatory: feel free to tinker around!

If you want e.g. comfycord/material/etc. support, you can edit the theme/template directly (e.g. in Vencord's "Open QuickCSS File") and import your favorite theme before the colors. Don't shy away from DIYing with the theme/template, it is not difficult.
