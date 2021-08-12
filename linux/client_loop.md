## To Fix these issues:
### client_loop: send disconnect: Broken pipe
### Connection reset by \<IP\> port 22

Add this to `~/.ssh/config`

```
Host *
    ServerAliveInterval 20
    TCPKeepAlive no
```

**TCPKeepAlive no** - *do not send keepalive messages to the server*

**TCPKeepAlive yes** - *client sends keepalive messages to the server and requires a response in order to maintain its end of the connection*. This will detect if the server goes down, reboots, etc. 

The trouble with this is that if the connection between the client and server is broken for a brief period of time (due to flaky a network connection), this will cause the keepalive messages to fail, and the client will end the connection with "broken pipe".

Setting TCPKeepAlive no tells the client to just assume the connection is still good until proven otherwise by a user request, meaning that temporary connection breakages while your ssh term is sitting idle in the background won't kill the connection.
