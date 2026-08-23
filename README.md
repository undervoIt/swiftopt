# SwiftOpt 
**Minecraft 1.20.1 · Fabric**

---

## What it actually does

Minecraft spends a lot of time rendering things that don't really need rendering — mobs way off in the distance, chests and signs across the map you're never looking at. SwiftOpt quietly skips those, which frees up your game to run better.

You stay in control of everything:

- **Entity culling** — stops drawing mobs, items, and other entities past a distance you set.
- **Block entity culling** — skips the "fancy" blocks (chests, signs, banners, beacons, etc.) once they're far enough away.
- **A live stats overlay** — see your FPS, frame time, and exactly how much is being skipped, in real time.
- **A settings screen** — flip things on and off, tune the distances, no config files required.
- **Safe Mode** — one switch turns all the culling off if you ever want vanilla behaviour back.

It doesn't touch how the world looks up close, and it doesn't change anything about gameplay.

## What it is NOT

Just so we're honest: this isn't Sodium. It won't replace Minecraft's whole rendering engine or magically triple your FPS. It's a focused, safe little mod that does a few useful things well. It plays nicely **alongside** Sodium, Iris, and Lithium if you use those too.

---

## Installing it

You'll need:

1. **Minecraft 1.20.1** with the **Fabric** loader ([get Fabric here](https://fabricmc.net/use/installer/) — pick 1.20.1).
2. **Fabric API** ([download](https://modrinth.com/mod/fabric-api) — grab the 1.20.1 version). SwiftOpt needs this to run.

Then:

3. Drop **`swiftopt-1.0.0.jar`** into your mods folder, next to Fabric API.
   - Windows: paste `%appdata%\.minecraft\mods` into your File Explorer address bar.
   - Mac: `~/Library/Application Support/minecraft/mods`
4. Launch the game using the **"fabric-loader 1.20.1"** profile.

That's it — no Java setup, no building, nothing else. The `.jar` just goes in the folder.

---

## Checking it works

Load into any world and type:

```
/swiftopt
```

If it prints a little status message, you're good. Then:

- Press **F6** to show the performance overlay.
- Press **O** to open the settings screen.
- Look at a bunch of mobs or chests, turn the distances down in settings, and watch the "culled" numbers climb.

If those numbers move, the mod is doing its job.

## Controls

| Key / Command | What it does |
|---|---|
| **F6** | Show/hide the stats overlay |
| **O** | Open the settings screen |
| `/swiftopt` | Show status |
| `/swiftopt overlay` | Toggle the overlay |
| `/swiftopt settings` | Open settings |
| `/swiftopt safemode` | Turn all culling off (or back on) |

Both keys can be rebound in **Options → Controls → SwiftOpt** if F6 or O clash with something else you use.

---

## If something looks off

- **A mob or chest vanished when it shouldn't have?** Your cull distance is set too low — bump it back up in the settings screen (press O), or just hit Safe Mode.
- **The "culled" numbers stay at zero?** The mod loaded but the culling isn't kicking in — worth flagging so it can be looked at.
- **Game won't start / says a mod is missing?** You're probably missing Fabric API, or you're on the wrong Minecraft version. It needs 1.20.1 + Fabric API, no exceptions.

Nothing here can corrupt your world — worst case, you toggle a setting off.

---

## License

MIT. That means you're free to use it, share it, and change it however you like — just keep the license file with it. Do whatever makes your game run better. 🙂
