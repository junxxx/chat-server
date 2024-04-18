A chat system build with Golang

1. group chat
   no need to register. Use a random user name.
   a chat room just a room id
   all clients in the same chat room can receive the messages sent from other client except the sender.
   So a message should have a propery from, to, and a room id

```
type Message struct {
   From  int (client)
   To    int (room-id)
   Content string
}
```
message flow:

client  ---->  chat room    ----> brodcast


```
type Room struct {
   Clients *Client
   Name string
}
```