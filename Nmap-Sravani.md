## Scanning

**Perform an active discovery analysis of the Pentesting VM using Kali VM (Nmap) to gather the following information. Use methods that minimize firewall detection, but do not worry about time and rate limit factors when constructing Nmap queries. (5 points)****
**
1. **IP Address and MAC Address of the Pentesting VM**:
   To find the IP address and MAC address of the Pentesting VM, you can run the following Nmap command:
   ```
   nmap -sn 10.0.2.0/24
   ```
   This will perform a simple ping scan (`-sn`), which will only determine whether the target is online and will provide you with the IP address and MAC address of the Pentesting VM = **10.0.2.15**.
%%    <Add_image_here> %%

2. **All open TCP ports on the Pentesting VM**:
   Use the following Nmap command to scan for open TCP ports:
   ```
   nmap -sT -p- -T4 10.0.2.15 --packet-trace
   ```
   This command will scan all 65535 TCP ports (`-p-`) aggressively (`-T4`) to find open ports on the Pentesting VM.

3. **All open UDP ports on the Pentesting VM**:
   Run the following Nmap command to scan for open UDP ports:
   ```
   nmap -sU -PS -p- 10.0.2.15 --packet-trace
   ```
   This command will scan all 65535 UDP ports to find open ports on 10.0.2.15. 

4. **Detect actual services and their respective versions**:
   Once you have identified open TCP and UDP ports, you can use Nmap's service version detection feature to determine the services running on those ports along with their versions. Use the following command:
   ```
   nmap -sV -p- 10.0.2.15 --packet-
   ```
   Replace `<open_ports>` with the list of open ports obtained from the previous scans.

5. **Operating System of the Pentesting VM**:
   To identify the operating system of the Pentesting VM, you can use Nmap's OS detection feature. Run the following command:
   ```
   nmap -O <Pentesting_VM_IP>
   ```


## Wireshark or --packet-trace
Regarding how Nmap collects this data using packet trace or Wireshark:

a. **Identify the IP Address and MAC Address**: 
Nmap sends out ARP requests and analyzes the responses to determine the IP and MAC addresses of hosts on the network.

b. **Identify an open TCP port**: 
Nmap sends SYN packets to various ports and analyzes the responses. If a SYN/ACK is received, it indicates an open port. if RST is received it is considered as closed port. Using packet trace we can deduce if a connection is successful (open) or refused (closed). Refer the below screenshot for reference.

c. **Identify an open UDP port**: 
Nmap sends UDP packets to various ports and analyzes the responses. If an ICMP port unreachable message is not received, it indicates an open port.

Here using `-PS` we are also sending TCP SYN packets to see if any ports responds to UDP and TCP SYN packets while running UDP scan. Refer the below screenshot

d. **Detect the service and service version on an open TCP port**: 
Nmap sends probes tailored to specific services and analyzes the responses to determine the service and its version. we use `-sV` to detect the services and their versions running. Nmap has its `nmap-services` database of about 2,200 well-known services, Nmap would report that those ports probably corresponding services like SMB, HTTP etc., Refer the below screenshot.

e. **Detect the specific operating system**: 
Nmap analyzes various aspects of network communication, including TCP/IP stack behavior and responses to specific probes, to make an educated guess about the target's operating system.