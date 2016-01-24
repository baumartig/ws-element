# ws-element
Wrapper for browser-native WebSocket client. It's built using the Polymer project.


## Usage


1. Import Web Components' polyfill:

    ```html
    <script src="bower_components/webcomponentsjs/webcomponents-lite.min.js"></script>
    ```

2. Import Custom Element:

    ```html
    <link rel="import" href="ws-element/ws-element.html">
    ```

3. Start using it!

    ```html
    <ws-element url="ws://localhost:9999" protocol="echo-protocol" on-open="onOpen" on-error="onError" on-message="onMessage"></ws-element>
    ```

## Options

Attribute       | Options                   | Default             | Description
---             | ---                       | ---                 | ---
`url`           | *string*                  | `undefined`         | WebSocket server endpoint to connect to.
`protocol`      | *string*                  | `undefined`         | A subset protocol to be used as part of the communication with the server.

## Methods

Method        | Parameters   | Returns     | Description
---           | ---          | ---         | ---
`send()`   | message String       |     | Used to send messages to the server.
`close()`   | None      |     | Close socket.

## Events

Event         | Description
---           | ---
`message` | Triggers when a message from the server is received.
`error` | Triggers when there is an error triggered by WebSocket client
`open` | Triggers when a socket is first open
