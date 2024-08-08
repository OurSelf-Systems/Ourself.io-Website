# A Self World

A Self world is a self-contained set of Self objects capable of running on a Self VM.

Self worlds can be snapshotted to disk.

Psyche hosts Self worlds in FreeBSD jails, then allows mediated access to them via a web browser, either to the console (REPL) or to the morphic desktop.

For Psyche's purpose, the on disk version of a Self world comprises a Self snapshot and some related files (eg config, also transporter sources etc.)

