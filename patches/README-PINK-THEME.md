# Pink Theme Patches for Loop

This folder contains patches to apply a complete pink color theme to Loop, replacing the default green/orange/teal colors with various shades of pink.

## Patch Files

### 1. `loop-pink-color-assets.patch`
**Module:** Loop
**Changes:** Updates 6 color assets in Loop/DerivedAssetsBase.xcassets:
- `insulin.colorset` - Hot pink (#ec4899)
- `carbs.colorset` - Light pink (#f472b6)
- `glucose.colorset` - Deep rose (#be185d)
- `fresh.colorset` - Pale pink (#fbcfe8)
- `warning.colorset` - Coral pink (#fda4af)
- `accent.colorset` - Deep rose for light mode, hot pink for dark mode

### 2. `loop-pink-critical-color.patch`
**Module:** Loop
**Changes:** Adds new `critical.colorset` for urgent/critical glucose alerts:
- Light mode: Deep magenta (#c2185b)
- Dark mode: Bright pink-magenta (#e6429b)

### 3. `loop-pink-code-changes.patch`
**Module:** Loop
**Changes:** Updates Swift code to use pink critical color:
- `LoopUI/Extensions/UIColor.swift` - Changes critical from systemRed to named color
- `LoopUI/Extensions/Color.swift` - Changes critical from red to Color("critical")

### 4. `loopkit-pink-insulin-gauge-colors.patch`
**Module:** LoopKit
**Changes:** Updates insulin gauge bar gradient colors used in preset screens:
- `Lightened Insulin.colorset` - Light pink (#f472b6)
- `Darkened Insulin.colorset` - Deep rose (#db2777)

### 5. `looponboarding-pink-welcome-icon.patch`
**Module:** LoopOnboarding
**Changes:** Updates the transparent loop icon on the welcome screen to pink gradient

### 6. `loop-pink-app-icons.patch`
**Module:** Loop
**Changes:** Updates all app icon sizes in Loop/DerivedAssetsBase.xcassets/AppIcon.appiconset/ with pink gradient loop icons (18 files)

### 7. `workspace-pink-app-icons.patch`
**Module:** Workspace (root level)
**Changes:** Updates all app icon sizes in OverrideAssetsLoop.xcassets/AppIcon.appiconset/ with pink gradient loop icons (18 files)

## Color Scheme Summary

### Glucose Display Colors
- **Normal (in-range):** Light/happy pink (#be185d)
- **Warning (low/high):** Medium coral pink (#fda4af)
- **Critical (urgent):** Dark pink/magenta (#c2185b)

### UI Element Colors
- **Insulin:** Hot pink (#ec4899) to deep rose gradient
- **Carbs:** Light pink (#f472b6)
- **Glucose chart:** Deep rose (#be185d)
- **Fresh data:** Pale pink (#fbcfe8)
- **Accent:** Deep rose

### App Icons
- Pink gradient loop (light pink to deep rose)
- Light gray gradient background
- All sizes from 20x20 to 1024x1024

## Installation Instructions

1. Upload all `.patch` files to your LoopWorkspace fork's `patches` folder
2. Commit the changes to your default branch
3. Run a browser build - patches will be automatically applied
4. The build will apply all patches in the order they're processed

## Notes

- These patches are compatible with Loop 3.4.0+
- All patches include proper module prefixes (Loop/, LoopKit/, LoopOnboarding/)
- Binary files (PNG images) are included as git binary patches
- The pink theme maintains visual hierarchy while providing a cohesive look

## Reverting

To remove the pink theme:
1. Delete all patch files from the `patches` folder in your fork
2. Commit the changes
3. Run a new browser build

---

Updated: October 22, 2025
