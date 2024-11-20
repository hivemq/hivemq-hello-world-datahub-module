# HiveMQ 'Hello World' DataHub Module Example
This repository contains a simple 'Hello World' example of a custom [DataHub Module](https://docs.hivemq.com/hivemq/latest/data-hub/modules.html#hivemq-modules-for-data-hub)
, intended for use with the [HiveMQ MQTT Broker](https://hivemq.com/).

This example is intended to show the files and metadata required to create a custom working module, as well as demonstrate how to implement some simple working Data Hub functionality using a custom module.  
This repo is also intended to be cloned and adapted for your own custom module needs, and to function as a basic starter template.

## Structure of the Custom Module

Custom modules must consist of a folder with the following files:

- `index.json`: This file contains the metadata for the custom module. It includes details that will be shown in the Control Center, such as the name of the module, a short description, and the version of the module.  It can also be used to set the the minimum HiveMQ Broker version required to use the custom module. It must also list the contents of the custom module.
- At least one [policy](https://docs.hivemq.com/hivemq/latest/data-hub/policies.html), referenced in the  `index.json` file. This can be either a data or behavioural policy. In this example, we show a simple data policy which validates if the incoming message is JSON and runs a short script to include a timestamp if this is the case. 
- All schemas and scripts referenced in the policy. 

## Import into the Broker

To import the custom module into your Broker, first zip the folder, including the files. This zip file can then be uploaded via Data Hub within the Control Center.

## Support

Full documentation for Custom Modules can [be found here](https://docs.hivemq.com/hivemq/latest/data-hub/modules.html#hivemq-modules-for-data-hub). For help or support in building your own custom modules, join [our community](https://www.hivemq.com/community/). 