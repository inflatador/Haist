# Haist. High.Altitude.Intercontinental.Server.Transmitter

Use this script to clone a Rackspace public cloud server to the same, or another datacenter. This is accomplished by building a new server of the desired flavor and size to the datacenter you choose. Both the original, and new servers are placed into rescue mode so that the original server's file system can be systematically cloned (block for block) using the linux command line utility, "dd".

The destination server's disk size must be the same size, or larger than the original server's disk. This script has "bumpers" which will prevent a smaller local disk, or block storage volume from being specified for the destination server.

Do you have an old Standard flavor server that you'd like to upgrade to a performance flavor like Compute, Memory, or I/O? Using Haist, this can be done with ease. No more fighting with images!

### RackConnect Support

At this time, only RackConnect v3 is supported, and only as the destination (not source). RackConnect v3 will eventually be supported as a migration source, and RackConnect v2 will eventually be supported as a migration source only.

## General Usage

Use __control.py__ to build the controller server. Next, login to the controller server and run __haist.py__, which does the actual migration work. (Or run control.py from your local computer which has SSH access to both source and destination. Either way, running in __screen__ or __tmux__ is highly recommended).
