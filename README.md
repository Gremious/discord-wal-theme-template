A pywal and [wallust](https://codeberg.org/explosion-mental/wallust) template for [Vencord](https://github.com/Vendicated/Vencord) (or probably any other client capable of loading css, no guarantees).

Does not modify any discord styling outside of colors - it is just a recolored, vanilla discord.

Is uses the same formula for generating background color shades as [Pywalfox](https://github.com/Frewacom/pywalfox/tree/master), so the colors will match :)

Dark theme only, sorry, I don't really use light themes, though it might work ok with `pywal -l`. If you edit the template because you use light themes with wal - feel free to PR!

## Usage

### pywal
Add this file to your `$HOME\.config\wal\templates` and there will be a `discord-wal.css` in your `$HOME\.cache\wal` when you run `pywal` (as per [https://github.com/dylanaraps/pywal/wiki/User-Template-Files](https://github.com/dylanaraps/pywal/wiki/User-Template-Files)).

You can then copy the cached theme to `$HOME\AppData\Roaming\Vencord\themes\wal.css` in the script you run to update things after running wal or w/e. Then you can enable it in the settings.

### wallust

Copy `discord-wallust.css` to `%appdata%\wallust`

Add 
```toml
pywalfox = { template = 'discord-wallust.css', target = 'C:/Users/UsernameAppData/Roaming/Vencord/themes/wallust.css' }
```
to your `%appdata%\wallust\wallust.toml`
Note that for toml, that *has* to be on one line. As an alternative, you can also write:

```toml
[templates]
[templates.vencord]
template = 'discord-wallust.css'
target = 'C:/Users/Gremious/AppData/Roaming/Vencord/themes/wallust.css'
```

---

I have left a bunch of notes and commented styles, and the color variable names are pretty self-explanatory: feel free to tinker around!

If you want e.g. comfycord/material/etc. support, you can edit the theme/template directly (e.g. in Vencord's "Open QuickCSS File") and import your favorite theme before the colors. Don't shy away from DIYing with the theme/template, it is not difficult.
