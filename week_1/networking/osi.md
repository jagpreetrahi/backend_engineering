## OSI Model

```
  1. It stands for Open System Interconnection Model.
  2. It break down the network communication into the seven abstract layers.
  3. Provide a standard for different computers to be able to communicate with each others.
```

Now we understand the seven layers of OSI model from the top to bottom.

- Application Layer : This is the layer where we interact and this is what we actually see or use it.
    Example : Brower and an email app.

- Presentation Layer : This layer is work as translator that helps to format the data like encrypt it , compress it , convert it into the format that the other side understand easily.
     

- Session Layer : This layer represent establishing, managing and terminating communication session.

- Transport Layer : It breaks the data into the segments, and make sure nothing is lost. This layer is responsible to add the port number.

- Network Layer : The GPS / router, It break segments into packets. This layer adds the IP addresses and it works seems from source to destination.
Example - Destination address on an envelope.

- Data Link Layer : It break down the packets into the frames. It handles link-local transmission and has a frame size limt. It adds tha MAC address. 
Example - Your Laptop and the Wi-Fi

- Physical Layer : It converts the everything into a raw bits streams and physically sends it via cable.
Example - Router, cables, wireless devices.

### Key notes 

```
Raw bits stream : Sequences of 0s and 1s - with no extra formatting, addressing 

The bits themselves abstract numbers, must be converted into some kind of physical signal that can travel through a medium.

1. Choose a medium i.e. cable, wireless
2. Converting the bits into a signal(radio waves, electric pulse) that matches a medium 
3. Send it over the medium 
4. Receiver decode it backs.


OSI is primarily a conceptual/reference model.

The modern Internet commonly uses the TCP/IP
(or Internet) protocol suite, whose layers do not
map perfectly one-to-one onto OSI's seven layers.

Use OSI to reason about responsibilities,
not as a literal diagram of every real network implementation.

```


