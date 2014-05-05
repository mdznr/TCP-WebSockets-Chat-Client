# TCP/WebSockets Chat Client

Write a chat client using HTML5, HTML5 WebSockets, CSS, and JavaScript. Use TCP/WebSockets to connect to the chat server. More specifically, you do not need to support UDP at all.
Your chat client must connect to the chat server on port 8787 (you may hardcode the server hostname and port number). When you submit your project, be sure the hostname is set to `localhost` and the port number is 8787. You might need to modify your Project #3 server to act as a WebSockets server.

Your chat client must validate as valid and well-formed HTML/CSS (i.e. HTML5 and CSS2 or CSS3). 
If your code does not validate, you will lose points.

When your client starts up, users must specify their username, which (once validated by the client) is sent to the server via a `ME IS` command. If an error occurs here (or elsewhere), use JavaScript `alert()` messages or some other means of displaying a dialog box to the user (which the user must acknowledge to close).

Once logged in successfully, the user is in the "main" interface. While the design is up to you, here are the minimum requirements:

1. Users must always be able to see their username in the upper-right hand corner of the page.
2. Users must always be able to click a LOGOUT button or link in the upper-right hand corner of the page to log out of the server.
3. Users must always be able to see a list of all users; refresh this list via the `WHO HERE` request (requested by the user via an UPDATE or REFRESH button/link). This must be in a separate column.
4. Messages sent via the "main" interface are sent to the chat server via the `BROADCAST command.
5. Usernames that appear anywhere in the interface should be highlighted in a persistent color (e.g. user X is shown in red, user Y is shown in green, etc.); cycle through at least 16 distinct colors).
6. When a user clicks on a username **ANYWHERE WITHIN THE "MAIN" INTERFACE**, the user interface opens a new window that allows the user to send and receive private messages. Likewise, when a private message is received, show it in a new window. If a window is already open for a given username, send and receive all messages from that window (i.e. do not blindly open a new window for each private message exchange).

No action by the user should cause the page to reload (i.e. avoid using "old-fashioned" forms that post request data to a server-side script). Use HTML5 and/or AJAX for this.

Your client must be able to accept asynchronous communication from the chat server. More specifically, the chat server may send any number of messages to the client at any time. You may assume that all messages are correct according to the protocol and rules specified in Project #3.

To test your client, network with your friends in class. Each of you can use a different client as long as one of you is running the chat server. You might also test by using multiple tabs/windows or even multiple browsers.

**Extra Credit**: Users must also be able to send image (or other) files to each other via private messages or broadcast. You may assume that all files sent are image files and will be uploaded by the client as a stream of bytes. Add the necessary browse and send buttons. When your client receives an image, display the image in a new window that frames the image and requires no scrollbars.

**Extra Credit**: Add support for inline images, meaning a client can send image data as part of their text (e.g. for emoticons).

**Important Note**: Other "bells and whistles" are nice, but please be sure your solution meets all the required specifications. Do not make changes to the protocol, unless you wish to lose points!