# Overview

Waves hand. *This is not the documentation you are looking for.*

(This is in fact some rough notes)

Psyche is a platform for running and accessing Self worlds.

From a technical perspective it is an integrated combination of Self and FreeBSD. It is provided as an ISO for an immutable OS which loads and then runs from memory. It should run on any machine which will run FreeBSD, although it is expected that most usage with be as a VM.

On first boot, a very simple installer guides the user through some key questions including setting up the zfs volume for storing Self worlds.

=> more about [Installing Psyche](installation/)

On subsequent boots, the machine console gives access to the console of a Self ‘control’ world which manages the system. A more friendly and usable interface is available in the form of access to the Control world’s desktop through a web browser.

Though the Control world, the operator is able to manage Self worlds and associated data. Worlds can be woken or put to sleep, imported or exported to snapshots, named, duplicated, deleted etc.

=> more about [The Control World](control/)

Access to each running world is through a web browser - no specific client software is needed. As such, users can access their Self programs from any modern computer including tablets and phones.

Each Self world comes with the facilities to allow multi-user access, allowing team development and use.

Running worlds are secure and separated from the rest of the system. The Control world can give them access to the Internet or deny them entirely. (<= not yet implemented)

=> more about [Self worlds](worlds/)
