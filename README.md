# Mythos Action Hub

Shared actions for Mythos Controller.

> **This library is part of the Mythos Controller project.** Its source of truth is the
> `hub-library/` folder of the main repository (`othoth77/mythos-controller`), reviewed and tested
> with the application. This repository is the **public copy** that installed applications read and
> where nominations are opened. Every change (publish, deprecate, withdraw, remove) is made in the
> main project and copied here with `tools/hub_sync.py push`; a change made here first (for example
> a publish from a clone of this repository) is brought back with `tools/hub_sync.py pull`.

* `index.json` – what the application reads (generated; do not edit by hand).
* `packages/<id>/<id>-<version>.mcaction` – one file per published version (never replaced).

## Proposing an action

In Mythos Controller open **Hub → Proposer**, choose the key to share and follow the steps: the
application opens a prefilled issue here in your browser. Nothing is sent before you submit it.

## Maintainers

    python tools/hub_publish.py review  <nomination file or issue text> --library .
    python tools/hub_publish.py publish <nomination file or issue text> --library .
    python tools/hub_publish.py reindex --library .

Every action is validated and scanned for secrets, but **read the code before publishing it**:
custom code runs with the user's Windows rights. Users always review an action before they
install it, and installed code stays inactive until they check and activate it themselves.
