# deep-map

[![ci](https://img.shields.io/github/workflow/status/mixphix/deep-map/Haskell-CI)](https://github.com/mixphix/deep-map/actions/workflows/ci.yml)
[![Hackage](https://img.shields.io/hackage/v/deep-map?color=purple)](https://hackage.haskell.org/package/deep-map)
[![license](https://img.shields.io/github/license/mixphix/deep-map?color=purple)]()

A `DeepMap` is a map that has several layers of keys.

```hs
type DeepMap :: [Type] -> Type -> Type
data DeepMap ks v where
    Core :: v -> DeepMap '[] v
    Wrap :: Map k (DeepMap ks v) -> DeepMap (k ': ks) v
```

For a given `(k ': ks) :: [Type]`, the type `DeepMap (k ': ks) v` is isomorphic to lists of the form `[(k, k0, .., kn, v)]` where `ks = '[k0, ..., kn]`, but with better performance.
