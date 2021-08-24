

<img src="https://upload.wikimedia.org/wikipedia/commons/e/e4/Tcp_state_diagram.svg">



## CLOSE_WAIT

- See in passive-close side
- Socket is waiting for the application to execute `close()`
- There is no way to close by OS, it has to be fixed by application itself

## TIME_WAIT

- See in active-close side
- It is normal to see (a lot of) `TIME_WAIT`
- By design, it takes time to wait before closing the socket
- For with high number of concurrent connections, socket may exhaust. It can be fixed by
  - Increase the port range that can be used for outbound connections
  - Decrease the time length for `TIME_WAIT`
  - Disable linger in web server
 
