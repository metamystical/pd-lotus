## pd-lotus
[lotus ] object for Pure Data - simple message database

### Description

[lotus ] stores messages in a database file in the format "key message-string", where the key is a symbol or number and message-string can have multiple elements separated by whitespace. The database file can be created and and edited outside of Pd but can also be updated from within Pd by sending a message to the active input of the [lotus ] object with the same format used in the database file, "key message-string". Each time the file is updated, it is resorted
according to the keys, one line for each message.

The database filename can be specified as a parameter when the object is created, like so: [lotus filename]. If the filename is left unspecified, it is set to 'db' by default. The database file must exist in the directory where the patch resides.

Stored message-strings are retrieved by sending messages to the active input of the [lotus ] object containing only a key (a symbol or number). If the passive input is toggled to '1', the message-string is removed from the database file rather than retrieved.

### Installation

The lotus.c file can be compiled into a Pure Data external using [pure-data/pd-lib-builder](https://github.com/pure-data/pd-lib-builder). Simply place the linked file (e.g. lotus.pd_linux) along with the help patch lotus-help.pd into the same directory as your patch, or somewhere on the Pd search path (e.g., externals/lotus folder).
