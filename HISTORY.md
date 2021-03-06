# Tomes Release Notes

## 0.2.3
 * Fixed: "typeChange" was always emitted when assigning objects or arrays (issue #48)
 * Fixed: another bug in V8 regarding enumerables was causing for-in loops to show too much (issue #43)
 * Minor performance improvements

## 0.2.2
 * Adds a workaround to a V8 bug exposing itself in JSON.stringify (issue #44)

## 0.2.1
 * Allow old snapshots to be passed to `takeSnapshot` as a high-performance shortcut.

## 0.2.0
 * Snapshot support

## 0.1.1
 * Suppressed the `_eventsCount` property of Node's EventEmitter

## 0.1.0
 * Removed the hide method, it was useless and only increased code complexity.
 * Added nodei.co badge.
 * Added node v0.11 back to travis, maybe it will work now.
 * unset executable bit from files.

## 0.0.22
 * inc now takes NumberTomes
 * Added this `HISTORY.md` file

## 0.0.21
 * IE9 support and travis fix for npm horribleness

## 0.0.20
 * toLocaleString does not work in browsers so we make a special one for them.

## 0.0.19
 * Tomes now behaves similar to JSON in that it throws a TypeError when it detects circular
   references in the data you passed to it. Tomes now does this on conjure and on unTome.

## 0.0.18
 * ArrayTome.indexOf and lastIndexOf now do a valueOf on the value to be searched for.

## 0.0.17
 * To avoid issues with multiple versions of Tomes not being able to recognize Tomes as Tomes,
   instanceof has been eradicated from Tomes. Instead we now check the to see if the constructor's
   name has Tomes in it. This is not perfect as Tomes will still fail to recognize Tomes from other
   iframes and windows. It's a step in the right direction regardless.

   Additionally, Tomes now has a readAll method to pull out the entire array of diffs from the root
   Tome. It seems like the vast majority of use cases always pull out all diffs, so this should
   improve performance there.
