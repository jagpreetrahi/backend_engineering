## TCP / IP model

### IP 

- It stand for the Internet protocol.
- It is kind of like a protocol, set of rules for routing and addressing the packets of data from source to the destination.
- It's only responsible for sending the data and hoping it arrives.
- It does not handle the packets ordering or error-checking.
- It is a connection less protocol means no idea about the previous packet or target does not send an ACK to the source.

```
TCP (Transmission Control Protocol) is used in conjuction with IP in oder to maintain a connection between the sender and the receiver, to ensure the packet order and no loss of data.
```

*** IP : Addressing & delivering system ***
                                       
*** TCP : Reliability & Ordering system ***  

#### How does it
```
Making sure each piece reahes the correct address - IP

Putting pieces back in the right order - TCP 

Asking for resend if a piece is missing - TCP 

Telling the sender "Get it" - TCP
```

### How TCP actually establish the connection - The 3- way hadnshake

Before sending any real data, TCP does a quick exchange.

1. SYN - Sender 
2. SYN-ACK - Receiver
3. ACK - Sender

#### Set of rules for IP 

1. Every device must have a unique IP address
2. Every packet must carry source and the destination IP.
3. Each packet is sent independently
4. Routers read only the destination IP with the help of IP information.
5. IP does not guarantee the delivery, order or error-checking.


#### Why need to handle the packet Ordering ??

Because packets can take differnet paths through the internet ( made up of millions of differenr networks/machines). If they don't reorder then it will be consider as garbage & the unreadable data.
So for this, attaching a sequence number to eack packet for re-ordering helps to gets back the same format of packets.


```
TCP breaks the data into segments; IP then wraps segments into a packets. The reason of breaking data down is as - 
  1. Networks can only carry the smaller chuncks at a time.
  2. Smaller chucks are easier to resend.
  3. Prevent one huge transfer from hogging the entire network.

```

#### If the receiver does not send the SYN-ACK then 
```
Connection never gets established

    1. Sender send SYN
    2. If no SYN-ACK come back within a certain time, sender retries - sends SYN again.
    3. This retry happend for a limited number of time.
    4. If still no response after multiple attempts - sender gives up and return the errors.
```

#### Do we need to do the handshake every time for the same destination ??

Often yes, but not always - connections can be reused

- Without reuse :  Every new TCP connection = new handshake 

- With reuse ( common in modern web/http ) : Once a TCP connection is open, it can be kept alive for multiple request.

#### If the packet is missing , does the TCP ask the sender using the same handshake ??
No, not the same handshake
It uses the same established connection.

(SYN - SYN_ACK - ACK) : happens once at the start to open the connection.
After that, TCP uses the sequence number with the ACk to track what's arrive.

