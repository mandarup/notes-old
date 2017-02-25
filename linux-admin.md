


# change swappiness to improve performance

https://community.linuxmint.com/tutorial/view/299

First, check the value of swappiness. Open terminal and type this command:

    cat /proc/sys/vm/swappiness

Temporarily change swappiness’ value to 10 using following command, and it will be reverted in next restart.

    sudo sysctl vm.swappiness=10

To permanently change this value, using:

    gksudo gedit /etc/sysctl.conf

Search for vm.swappiness and change its value as desired. If vm.swappiness does not exist, add it to the end of the file like so:

    vm.swappiness=10
