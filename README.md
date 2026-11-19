# Mythos Action Hub

Shared actions for Mythos Controller.

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
