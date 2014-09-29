# Multicast Docker PoC

**_Testing multicast with R/S docker images_**


To Build 
```
cd Receiver
docker build -t fedora/recv .
cd ..
cd Sender
docker build -t fedora/send .
```

To Run

1st terminal 
```
$> docker run -t fedora/recv
------------------------------------------------------------
Server listening on UDP port 23364
Binding to local address 224.0.1.105
Joining multicast group  224.0.1.105
Receiving 1470 byte datagrams
UDP buffer size:  208 KByte (default)
------------------------------------------------------------
[  3] local 224.0.1.105 port 23364 connected with 172.17.0.27 port 40058
[ ID] Interval       Transfer     Bandwidth        Jitter   Lost/Total Datagrams
[  3]  0.0- 1.0 sec   128 KBytes  1.05 Mbits/sec   0.024 ms    0/   89 (0%)
[  3]  1.0- 2.0 sec   128 KBytes  1.05 Mbits/sec   0.013 ms    0/   89 (0%)
[  3]  2.0- 3.0 sec   128 KBytes  1.05 Mbits/sec   0.064 ms    0/   89 (0%)
[  3]  0.0- 3.0 sec   386 KBytes  1.05 Mbits/sec   0.058 ms    0/  269 (0%)
```

2nd terminal
```
$> docker build -t fedora/send
------------------------------------------------------------
Client connecting to 224.0.1.105, UDP port 23364
Sending 1470 byte datagrams
Setting multicast TTL to 32
UDP buffer size:  208 KByte (default)
------------------------------------------------------------
[  3] local 172.17.0.27 port 40058 connected with 224.0.1.105 port 23364
[ ID] Interval       Transfer     Bandwidth
[  3]  0.0- 1.0 sec   129 KBytes  1.06 Mbits/sec
[  3]  1.0- 2.0 sec   128 KBytes  1.05 Mbits/sec
[  3]  2.0- 3.0 sec   128 KBytes  1.05 Mbits/sec
[  3]  0.0- 3.0 sec   386 KBytes  1.05 Mbits/sec
[  3] Sent 269 datagrams

```


