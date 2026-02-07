# Content Architecture Patterns

## Feature-First Organization
- Each gameplay variant lives in its own folder (example: `Variant_Combat`).
- Feature folders contain their own Level, Blueprints, and assets.
- Shared assets live at the root and are reused by multiple features.

## Feature Folder Layout
Typical layout inside a feature folder:
```
Variant_Feature/
  Anims/
  Blueprints/
  Input/
  Materials/
  UI/
  VFX/
  Lvl_Feature.umap
```

## Blueprint Organization
Inside `Blueprints/`, use subfolders to keep classes clear:
```
Blueprints/
  Actors/
  Components/
  Interfaces/
  Systems/
  UI/
```
Use this when a feature grows beyond a few files.

## Level Ownership
- Each feature owns its own Level file.
- Levels should not pull feature-specific assets from other features.

## Dependencies
- Allowed: Feature -> Shared
- Avoid: Feature -> Feature
- Avoid: Circular references across features

## Unreal Generated Data
- `__ExternalActors__/` and `__ExternalObjects__/` are generated and tracked by Unreal.
- Do not create assets manually inside these folders.

