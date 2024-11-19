# Revision history for deep-map

## 0.3.1

* fix recursive definition of `mapMaybe`
* add `filterWithKeys` and `partitionWithKeys`

## 0.3.0

* rename constructors and patterns
* add support for `witherable` classes
* add `mapMaybeWithKeys` and `mapEitherWithKeys`

## 0.2.0.1

* Update copyright and re-trigger Hackage build with newer ghc

## 0.2.0

* Heterogenous list `type Deep :: [Type] -> Type` to increase compatibility with `indexed-traversable`. Requires an `Ord` constraint upfront to construct any nontrivial values.
* related `_Deep` functions

## 0.1.1.0 -- 2021-12-07

* Strict variants of `foldMapWithKey(N)`

## 0.1.0.0 -- 2021-11-30

* Deep monoidal maps
