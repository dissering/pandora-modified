# Pandora

Customized Pandora UI library with a compact, logo-free horizontal-tab layout.

- Default accent: `#FCDC5A`
- Tabs: text-based (for example, Combat, Visuals, Misc, Settings)
- No `Configs` directory or manual profile controls
- Settings are loaded from and automatically saved to `Pandora/settings.json`
- The Settings tab exposes accent, background, surface, element, border, text, and inactive-text colours

Use a named page and a title when creating the window:

```lua
local Window = Library:Window({
    Title = "Window",
    Build = "developer"
})

local Combat = Window:Page({Name = "Combat"})
local Visuals = Window:Page({Name = "Visuals"})
local Misc = Window:Page({Name = "Misc"})
Library:CreateSettingsPage(Window, KeybindList, Watermark)
```

The bundled `Example.lua` contains a complete four-tab example. If you serve the library over HTTP, publish this customized `Library.lua` first; the original upstream raw URL continues to serve the upstream version.
