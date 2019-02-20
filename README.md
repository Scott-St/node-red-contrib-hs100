# node-red-contrib-hs100

Note: This just has some minor changes to support my nodered installation design.

Original Description Below:


This Node-RED node is for controlling tp-link Wi-Fi Smart Plug - Model HS100.

This node has only been tested with a HS100(UK). The HS100 is also available in US and EU plug
versions. We expect they will work too.

This node simply wraps the excellent work here https://github.com/czjs2/hs100-api.

# Installation

Change directory to your node red installation:

    $ npm install node-red-contrib-hs100

Alternatively, use the Palette Manager in Node-RED.

# Configuration

Drag this node on to a worksheet and double click it. Enter the IP address of the plug on your
network. Save and deploy.

# Actuations

This node supports a number of actuations that are invoked by sending a msg.topic or msg.payload
to the node's input.

| Topic/Payload      |                                     Description                                      |
| ------------------ | :----------------------------------------------------------------------------------: |
| on                 |                                To turn the HS100 on.                                 |
| off                |                                To turn the HS100 off.                                |
| info               | Get all plug info, combination of sysinfo, cloudinfo consumption, schedulenextaction |
| sysinfo            |                            Get general plug information.                             |
| cloudinfo          |                            Get TP-Link Cloud information.                            |
| consumption        |                              Get power consumption data                              |
| powerstate         |                             Returns true if plug is on.                              |
| schedulenextaction |                                                                                      |
| schedulerules      |                                                                                      |
| awayrules          |                                                                                      |
| timerrules         |                                                                                      |
| time               |                                                                                      |
| timezone           |                                                                                      |
| scaninfo           |                                                                                      |
| model              |                                                                                      |

## Turn on

## Turn off

## Obtain power consumption data

To obtain the power consumption, send a message to this node's input with the topic or payload
set to `consumption`. The consumption data will be sent via this node's output in `msg.payload`.
