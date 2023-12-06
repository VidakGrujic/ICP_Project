 # ICP_Project

This is a team project from the course Industrial Communication Protocols done by Nikola Tanovic and Vidak Grujic

**Programming language: C/C++**

## Descritpion

The task was to made distributed server-client application, where data from the server are distributed between clients. In order to collect all data, client had to refer to the server and to the rest of the client. 
Communication server-client and client-client is implemented as TCP protocol, using the multithreading. 

### Implementation

On the server, files are stored in form of the long string. In one thread, server activates listen socket, waiting for clients to connect. Every connection to the client is done through new socket and new thread. The reason for multithreading is to optimize work of the server. 

