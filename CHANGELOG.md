## 1.0.0-dev.9

### Include binaries for Android and Windows to streamline usage
- Add `libzmq` binaries for Android
- Add `libzmq` binaries for Windows
- Add counter to example and ip address of host machine


## 1.0.0-dev.8

### Remove flutter dependencies
- Remove flutter dependencies (`environment`, `sdk`, `flutter_test`, `flutter_lint`)
- Bump example dependencies


## 1.0.0-dev.7

### Minor documentation improvements
- Fix rename of `SocketMode` to `SocketType` in README
- Add receiving messages (`ZMessage`, `ZFrame` and payloads) to README and example
- Override `toString` function in `ZMessage` and `ZFrame` for better debugging experience


## 1.0.0-dev.6

### Free pointers before throwing a ZeroMQException
- Free pointers before throwing a ZeroMQException
- Add return code to `zmq_setsockopt` function
- Add return code check to `ZSocket.setOption` function
- Add `zmq_has` function for checking supported capabilities
- Add helper functions for `zmq_has`


## 1.0.0-dev.5

### Fix destroying poller and loading shared library
- Rename `SocketMode` to `SocketType`
- Add some steps on how to use dartzmq on Android
- Address warnings in bindings.dart
- Fix destroying poller (use **poller instead of *poller)
- Add more class documentation
- Fix loading shared library for orher platforms
- Extend error messages
- Add more socket options


## 1.0.0-dev.4

### Fix heap corruption due to wrong usage of `malloc.allocate`
- Use periodic timer to poll sockets every second
- Poll all messages on socket instead of one for each event to not loose messages
- Reuse zeromq message pointer
- Improve return code handling
- Rename `_isActive` of `ZContext` to `_shutdown`
- Rename `_handle` and `_zmq` of `ZSocket` to `_socket` and `_context`
- Add stream for `ZFrames` to `ZSocket`
- Always show error code in `ZeroMQException`
- Fix pubspec of example


## 1.0.0-dev.3

### Add example, subscriptions for `sub` sockets and code cleanup
- Add minimal working example
- Rename `ZmqSocket` to `ZSocket`
- Rename `ZeroMQ` to `ZContext`
- Rename `ZeroMQBindings` tor `ZMQBindings`
- Add `subscribe(String topic)` and `unsubscribe(String topic)` to manage subscriptions of `sub` sockets


## 1.0.0-dev.2

### Add support for multipart messages
- Rename `Message` to `ZFrame`
- Add `ZMessage` as a queue of `ZFrame`'s
- Receive messages as `ZMessage` instead of `Message`(`ZFrame`)
- Reduce minimum SDK version to `2.13.0`


## 1.0.0-dev.1

### Add crude implementation of libzmq
- Creating sockets (pair,  pub,  sub,  req,  rep,  dealer,  router,  pull,  push,  xPub,  xSub,  stream)
- Sending messages (of type `List<int>`)
- Bind (`bind(String address)`)
- Connect (`connect(String address)`)
- Curve (`setCurvePublicKey(String key)`, `setCurveSecretKey(String key)` and `setCurveServerKey(String key)`)
- Socket options (`setOption(int option, String value)`)