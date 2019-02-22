# iperf
## IPERF commands cheat sheet created for the audit video for Cybrary
- Download and install on Centos (RPM based systems):  
`wget https://iperf.fr/download/fedora/iperf3-3.1.3-1.fc24.x86_64.rpm`
- Run as a server listening on UDP/TCP port 5201:  
`iperf3 -s`
- Run TCP test with default parameters (run on client):  
`iperf3 -c <IP address of the server>`
- Run the default TCP test but in reverse direciton:  
`iperf3 -c <IP address of the server>  -R`
- Run UDP test setting desired throughput to 10 Mbit/sec, first from client to server, then in opposite direction:  
`iperf3 -c <IP address of the server> -u -b 10M`  
`iperf3 -c <IP address of the server> -u -b 10M  -R `  
- Run TCP test for 120 seconds:  
`iperf3 -c <IP address of the server>  -t 120`
- Run TCP test using custom port of 10443:
Server: `iperf3 -s -p 10443`
Client: `iperf3 -c <IP address of the server>  -p 10443`
- Run TCP test with 5 simultaneous sessions:
`iperf3 -c <IP address of the server>  -P 5`


