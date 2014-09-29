# Multicast Docker PoC

**_Testing multicast with R/S docker images_**


To Build 
```
cd Receiver
docker build -t fedora/recv
cd ..
cd Sender
docker build -t fedora/send
```

To Run

1st terminal 
```
docker run -t fedora/recv
```

2nd terminal
```
docker build -t fedora/send
```


