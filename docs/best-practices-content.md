# Best Practices for Content

## Organization
- Keep assets local to the feature that uses them.
- Use `Shared/` only when an asset is reused by 2+ features; otherwise keep it inside the feature.
- Use `LevelPrototyping/` for throwaway tests and experiments.

## References
- Prefer soft references when practical to reduce hard coupling.
- Avoid cross-feature references.
- Clean up redirectors after moving assets.

## Materials and Textures
- Use `MI_` Material Instances instead of duplicating `M_` base materials.
- Keep textures next to the materials that use them when feature-specific.

## Blueprints
- Keep Blueprint graphs small and focused.
- Split large logic into components or helper Blueprints.
- Use consistent naming for variables and functions.

## Levels
- One feature, one level, unless there is a clear reason to split.
- Keep Level-specific assets inside the same feature folder.

## Source Control Hygiene
- Avoid renaming many assets at once.
- Commit asset moves and refactors in small batches.
- Keep Collections updated for active work areas.
