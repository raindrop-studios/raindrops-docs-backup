# Installation

The Boot-Up CLI is part of the Raindrops protocol.  Install the Raindrops CLI using the instructions [found here](../../../quick-start.md#install-the-cli), the Boot-Up CLI is included in the `raindrops-cli`.  Once installed, you will have access to a sample configuration file which works with the Degenerate Trash Panda collection.

To find this, use the following commands:

`npm list -g`&#x20;

To find the location of the raindrops CLI on your machine.  You will get something similar to the following:

`/Users/<your user name>/.nvm/versions/node/v18.8.0/lib`

Once you are in the directory specified, make your way to the boot-up example-configs directory, located at

`node_modules/@raindrops-protocol/raindrops-cli/example-configs/boot-up`

Rename the pandaExample.json file to reflect your project name and move it to the desired working directory

`mkdir ~/boot-up`

`cp ./pandaExample.json ~/boot-up/myProject.json`

This file establishes the definition of the boots-enabled configuration of the collection. You will want to keep this file safe, saving often as you go through this process because as you boot-up your collection the configuration is updated with on-chain ids and other configuration items that will be important to complete the process.

Let's have a look at the keys in the configuration file and what they mean
