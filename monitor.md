# Monitoring interfaces within the experiment

Scripts built on top of tcpdump and wireshark can be used to monitor different
interfaces on different servers in the experiment.

Login to different servers and run the `start_capture.sh` script with the interface to be debugged:

    sudo /local/repository/bin/start_capture.sh <interface>

On a separate server which has wireshark use the `monitor.sh` script to view the packet dump from
all the servers where you started the capture.

You will need to configure the server ip and username in `interface_list.conf` and run as follows:

    sudo ./monitor.sh interface_list.conf

Sample `interface_list.conf` is present in the repository.
