A wal template for [Vencord](https://github.com/Vendicated/Vencord) (or probably any other client capable of loading css, no guarantees).

Does not modify any discord styling outside of colors - it is just a recolored, vanilla discord.

Is uses the same formula for generating background color shades as [Pywalfox](https://github.com/Frewacom/pywalfox/tree/master), so the colors will match :)

Dark theme only, sorry, I don't really use light themes, though it might work ok with `pywal -l`. If you edit the template because you use light themes with wal - feel free to PR!

## Usage

Add this file to your `$HOME\.config\wal\templates` and there will be a `discord-wal.theme.css` in your `$HOME\.cache\wal` when you run `pywal (as per [https://github.com/dylanaraps/pywal/wiki/User-Template-Files](https://github.com/dylanaraps/pywal/wiki/User-Template-Files))

Until Vencored closes https://github.com/Vendicated/Vencord/issues/614, I recomend copying the cached theme to `$HOME\AppData\Roaming\Vencord\settings\quickCss.css` in the script you run to update things after running wal or w/e (be mindful of overrides if you use css snippets).

If you want e.g. comfycord/material/etc. support, you can edit the theme/template directly (e.g. in Vencord's "Open QuickCSS File") and import your favorite theme before the colors. Don't shy away from tinkering with the theme/template, it is not dificult.
