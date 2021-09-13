# Node Stats & Alerts

For individuals or groups contributing space to the cluster, Arken implements an optional statistics and alert system called [Arkstat](https://github.com/arken/arkstat) to help visualize the state of the cluster. When enabled, nodes periodically send Arkstat the amount of data they are willing to contribute as well as the size of the files they are already backing up. This data is inturn used to show the usage diagram on the [arken.io](https://arken.io) website as well as help us at Arken make decisions about which data we can accept into the Arken cluster.

In the case that a user also provides their email when setting up their node, Arkstat can also act as an alert system which will send the user an email when their node disconnects from the cluster for longer than a day. Upon alerting a user that their node is offline Arkstat immediately deletes the user's data from the stats database for security and to protect your privacy.
