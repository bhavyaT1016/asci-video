Inspiration

During our Data Structures and Algorithms class, we learned about Huffman encoding and obtaining pixels from an image. We wanted to see if it was possible to send an ASCII character feed as a replacement for a traditional video feed. We theorize it uses less data than a traditional video feed since all the encoding is done client-side; what's sent over the network are single 8-bit ASCII characters in place of many 24-bit pixels.

What it does

Converts your webcam video stream to an ASCII video stream, and broadcasts that ASCII stream to a socket.io server to be viewed by others online.

Client: Analyze your webcam feed, and do the following for video every frame (in order):

Grab pixel data from the screen

Calculate the color of each pixel

Compute contrast factor: Increase/decrease the brightness of each pixel to improve ASCII representation

Calculate the brightness value of each pixel

Assign an ASCII character to each pixel according to their brightness value.

Connect to socket.io server

Emit a chat message to the socket.io server containing the built ASCII frame for the video (every 50ms)

Server: Displays the ASCII video feed;

Receives ASCII video frames from client

Displays the latest ASCII video frame on an HTML page.


How we built it

We used JavaScript, Node.js, socket.io, ngrok, and Express.js. We created two separate projects, client and server which are frontend and backend respectively. Both are Node.js and Express.js based. The client converts the webcam feed to ASCII, and sends it to the server. The server receives the feed from the client and displays it. Anyone online with the link to the server can view the feed. We used ngrok to tunnel directly to one computer for demo purposes.

Challenges we ran into

Everything

Actually reliably computing the ASCII video feed was really tough, luckily we were able to find some examples online to go off of

Connecting the feed to the socket server, we had to use ngrok which lets us tunnel a connection from one computer to another temporarily.

Properly displaying the feed on the screen.

Accomplishments that we're proud of

Just that we got it working, we just wanted to see if it's possible.


What we learned

Servers and networking are really complicated

ASCII-based video feeds aren't half bad!

What's next for HackRU Spring 2022 ASCII Video Feed

We'd love to add full peer-to-peer connections so we can have both parties view their video feeds and realtime side-by-side comparison on data usage.


Team Information

Bhavya Tyagi 

Michael Palladino 

Jonathan Davies

Deep Patel
