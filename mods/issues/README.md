# /mods/issues — shared issue-tracker landing page

Modrinth requires an `https://` URL in the "Issue tracker" field. Rather than putting a
repository link on the listing, every mod points here and this page forwards users on.

## URL to paste into Modrinth

```
https://brennan.games/mods/issues/?mod=<slug>
```

Current slugs: `keeptrim`, `ediblebackpacks`. No/unknown slug shows a hub listing every mod.

## Adding a mod

Add one line to `MODS` in `index.html`:

```js
myslug: { name: 'My Mod', repo: 'bh679/mymod-mc' },
```

The tracker URL is built in JavaScript at runtime on purpose — keep repository links out
of the HTML markup and out of any server-side redirect.
