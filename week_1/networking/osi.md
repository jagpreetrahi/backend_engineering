## OSI Model

```
  1. It stands for Open System Interconnection Model.
  2. It break down the network communication into the seven abstract layers.
  3. Provide a standard for different computers to be able to communicate with each others.
```

Now we understand the seven layers of OSI model from the top to bottom.

- Application Layer : This is the layer where we interact and this is what we actually see or use it.
    Example : Brower and an email app.

- Presentation Layer : This layer is work as translator that helps to foramt the data like encrypt it , compress it , convert it into the format that the other side understand easily.
    Example : Sending a whatsapp message to someone, before it, gets to encrypt it. 

- Session Layer : This layer is called as conversation manager. It opens the connections for the two devices/network, keep it alive while talking and closed  when it's done.

- Transport Layer : It breaks the data into the segments, and make sure nothing is lost. This layer is responsible to add the port number that ensure the data reaches to the right app and also error-checking.

- Network Layer : The GPS / router, It break segments into packets and find the best route across the different networks. This layer adds the IP addresses and it works seems from source to destination.
Example - Destination address on an envelope.

- Data Link Layer : It break down the packets into the frames. Frames has the size limit so we don't directly send the large file over it. It handles the communication between devices on the same local network. It adds tha MAC address. 
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


