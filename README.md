# Jeopardy Loot Filter

Personal RuneLite Loot Filters project, based on the Rikten-derived filter selected in the saved Jeopardy profile.

[GitHub repository](https://github.com/jeopardy-brooks/jeopardy-loot-filter) · [Raw filter URL for import](https://raw.githubusercontent.com/jeopardy-brooks/jeopardy-loot-filter/main/filter.rs2f)

## Files

- `filter.rs2f`: working custom filter; displayed as **Jeopardy Custom Loot Filter**.
- `baseline/riktenx-jeopardy-value-sort.rs2f`: exact starting copy for comparison and recovery.
- `PROVENANCE.md`: source and verification details.

The initial working filter changes only the display name. It preserves all existing modules, item lists, colors, GE-value pickup-menu priority tiers, and the Superior dragon bones visibility/color exceptions. RuneLite profile settings (including separate hidden/highlighted lists) are not included in this filter.

## Import and customize

1. Copy the **Raw filter URL for import** linked above.
2. Open [Loot Filters UI](https://loot-filters.kaqemeex.net), choose the filter import action, and import from that URL.
3. Select **Jeopardy Custom Loot Filter** and adjust its modules.
4. Export the configured filter using the site's export controls. Import/select it in RuneLite Loot Filters on the Jeopardy profile. If placing a file in the plugin's filters directory manually, reload filters from disk before selecting it.
5. Verify the result in game before replacing your usual selection.

A public repository supports the documentation's unauthenticated raw-URL import workflow. For a private repository, use a local file import if supported by the UI; do not put GitHub credentials into an import URL.

## Development

Edit `filter.rs2f`, keeping structured `/*@ define:module:... */` and `/*@ define:input... */` comments alongside the relevant definitions. Preserve rule order: later assignments and terminating rules can affect behavior. Keep `baseline/` unchanged so changes remain easy to compare.

Commit and push intentional changes. The editor may cache the remote source for a few minutes before its update action becomes available. UI-only changes should be exported and deliberately brought back into the repository if you want GitHub to retain them.

Reference: [Modular Filters book](https://github.com/Kaqemeex/loot-filters-ui/tree/main/module-system-docs/modular-filters-book).

## Status

Starter published to GitHub. Editor import and in-game activation have not yet been verified. The original installed filter and RuneLite profile have not been modified.
