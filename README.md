 # ICP_Project

This is a team project from the course Industrial Communication Protocols done by Nikola Tanovic and Vidak Grujic

**Programming language: C/C++**

## Descritpion

The task was to made distributed server-client application, where data from the server are distributed between clients. In order to collect all data, client had to refer to the server and to the rest of the client. 
Communication server-client and client-client is implemented as TCP protocol, using the multithreading. 

### Implementation

On the server, files are stored in form of the long string. In one thread, server activates listen socket, waiting for clients to connect. Every connection to the client is done through new socket and new thread. The reason for multithreading is to optimize work of the server. Then, client sends the ID of the string which part it wants and number of bytes it wants to store. After recieving request, server sends to client data about the other clients which store the parts of that file. Data includes IP adress and port of client for every part and also number of bytes stored. In case there is a part of a file which is not distributed to other clients, server sends that part of the file directly. After getting response, client must refer to other clients and collect file's parts. When clients collects all parts, then it has to concatenate parts and show the string on the commmand promt. Also, clients have their listening and accepting sockets, the former wait for other client's connections and later for communication with the server. 
