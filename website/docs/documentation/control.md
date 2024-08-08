# The Control World

Though the Control world, the operator is able to manage Self worlds and associated data. Worlds can be woken or put to sleep, imported or exported to snapshots, named, duplicated, deleted etc.

## Outline of Main Objects in Control World

`psyche` is the main entry point and contains the main boot routine.

`psyche sys` is a wrapper around the underlying FreeBSD OS. Mostly this wraps the command line. Included are `jails`, `zfs` and so on. Most objects in the Pysche system include a link to `psyche sys`. Objects should not call out to the OS other than through `psyche sys` and ideally will keep their use of `psyche sys` as high level as possible (eg limit use of `sys sh: ''`)

`psyche worlds` handles the various Self worlds stored on the system. Worlds are stored as snapshots in the root directory of a dataset under `/worlds/store/1234-1234-uuid/`. Interact with Worlds by obtaining a `psyche worlds worldRecord` which is an immutable, updatable record of the World at a particular timestamp. Worlds may be started, stopped, deleted etc.

Key methods:

- `psyche worlds updatedSystemRecord` gets a record of the system status
- `aSystemRecord knownWorlds` returns a set containing world records of each world known to the system
- `aWorldRecord updatedWorldRecord` gives you a new updated record.

With a worldRecord there are then:

- `wake`
- `sleep`
- `delete`
- `duplicate`
- `duplicateURL: aURL`

