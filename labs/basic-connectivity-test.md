# Lab 1: Basic Network Connectivity Test

## Objective
To verify that a computer can connect to the local
network and the internet.

## Commands Used

### ipconfig
Used to view the IP address assigned to the computer.

## Observations
The Ethernet adapter showed "Media disconnected", indicating no cable connected.
A virtual Ethernet adapter had an IP address but no default gateway, meaning no internet access.
The active WiFi adapter had a private IPv4 address and a default gateway.
The presence of a default gateway confirmed internet connectivity.

## Conclusion
The system is connected to the internet via the WiFi adapter.
Only the adapter with a valid default gateway provides internet access.

### ping 8.8.8.8
Used to test connectivity to an external IP address.

##observation 
all 4 sent packets were recived(0% loss)

### tracert google.com
Used to trace the path packets take to reach a website

## Observations
- Hop 1 showed the default gateway, confirming the local network exit point.
- Some hops returned "Request timed out", indicating ICMP was blocked while traffic was still forwarded.
- Multiple hops used private IP addresses (10.x.x.x), showing traversal through the ISP’s internal network.
- ISP hostnames resolved, confirming the traffic passed through the Vodacom backbone.
- Final hops reached Google-owned IP addresses, confirming successful end-to-end connectivity.

##final results

- The computer received a private IP address.
- Ping responses were successful.
- Traceroute showed multiple hops.

## Conclusion
The device has working network connectivity.
