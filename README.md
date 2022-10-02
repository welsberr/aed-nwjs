# aed-nwjs

Avida-ED-Eco in NW.js

## Initial pass ##

This is the start of experimenting with use of NW.js to
package the Avida-ED-Eco web app for deployment to multiple
host platforms while keeping a fixed browser so that
the version as it stands can have long-term stability
for use into the future.

## Prerequisites ##

To develop and build the project, the Node Package Manager (npm)
is needed. Install that as appropriate to the host OS.

## Organization ##

This top-level directory contains two necessary files:

* .npmrc
* package.json

The Avida-ED-Eco directory contains one necessary file:

* package.json

The contents of the Avida-ED-Eco Git repository must be
added to the Avida-ED-Eco directory.

## Operations ##

The project dependencies need to be installed.

In the top-level directory, run:

> npm install

Once that successfully completes, a development
session can be invoked with:

> npm run dev

That launches an instance of the Chromium browser
with Avida-ED-Eco/index.html loaded in it. The SDK
build version of NW.js is specified in the
configuration file .npmrc, and the Devtools window
can be invoked In Windows or Linux by pressing F12
or <ctrl-shift-J>.

Once development is complete, building for deployment
can be invoked as:

> npm run prod

## Issues ##

1. There is incomplete loading of libraries. The Dojo
libraries fail on a parse task.

2. It appears that there are additional steps needed
to set up proper WebWorker use for avida.js in the Node context.

