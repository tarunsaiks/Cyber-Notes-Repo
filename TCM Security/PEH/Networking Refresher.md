# IP Addresses

- Ip addresses are used to communicate over Network layer (layer 3 of OSI model).
- Two versions of IP Addresses - IPv4 and IPv6

```
$ifconfig
```

output of ipconfig has inet and inet, which indicate ipv4 and ipv6 respectively.

## IPv4
- IPv4 are 32-bit numerical addresses represented in dotted decimal format. (192.168.29.1)
- Each section in IPv4 is called octet and consists of 8 bits and can range from 0 to 255 (8bit x 4 dotted decimals = 32bit)
- Total number of unique addresses sizes up to 2^32 (4.3 billion)
- Due to rapid growth of internet and multiple devices with each person and IoT, the number of IPv4 addresses has become limited.
- Private and Public IP address are different in usage.
- A **private IP address**, such as a home or office network, is assigned to a device on a local network and is used to identify the device within that network. 
- A **public IP address** is assigned to a device directly connected to the internet and is used to identify the device on the internet.

![[Public-vs-Private-IP-Addresses-01-EN.webp]]

## IPv6
- IPv6 are 128-bit addresses represented in hex
- Size approx. 3.4x10^38.
- IPv6 addresses are divided into eight groups of four hexadecimal digits, separated by colons. 
- Leading zeros within a group can be omitted, and consecutive groups of zeros can be represented by a double colon (::) to simplify the address.

