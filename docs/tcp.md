# TCP scenarios

Three-way handshaking.

## Active open (client `connect`s)

Step 1: `connect()` sends `SYN`, see [here](syscall.md#connect)

Step 2: receives `SYN+ACK` from server, sends `ACK`.

## Passive open (server `accept`s)

First, call [`bind()`](syscall.md#bind) and [`listen()`](syscall.md@listen) to setup the server.

Step 1: Receives `SYN` from client, sends `SYN+ACK`

Step 2: Receives `ACK` from client

Then we can [`accept()`](syscall.md#accept).
