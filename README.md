
 # mio-meta
 
 Here in mio-meta, you will find the tools and configuration files necessary to bootstrap deployment of devices. 
 There are examples of mio meta data and interfaces. For more inoformation about the Sensor Andrew schema visit
 the schema [github page](https://github.com/WiseLabCMU/sa-schema).

## Installation

First install [libmio](https://github.com/WiseLabCMU/libmio). This will require autotools and a few other 
dependencies. 


## Usage

<pre><code>
./meta_tool -n [device name] -type [device type] -id [node_id] -u [username] -p [password] -t [parent uuid in tree] -a [add reference to child 1 or 0] -acm [access control model]
    device name - the name of the device, stored in device meta information.
    type (optional) - The type of meta information to include in the device. Phillips Hue, Lutron Area Etc. If none of these, assumes it is a uuid and checks for the meta data of an event node. If that metadata is found, it copies it.
    node id - The Event node id of the device.
    username - username of device creater
    password - password associated with device creator
    paren uuid (optional) - the uuid of the reference node to add new event node id to.
    add refference to child (optional) - if 1 adds reference from child event node (the created event node), to the parent event node
    acm (optional) - access control model to use for the event node. Default open
</code></pre>
