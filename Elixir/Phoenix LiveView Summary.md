# Phoenix LiveView
A summary for Phoenix LiveView.

## Phoenix

### Flow CRC pattern

Phoenix follows the pattern **CRC** (Constructors Reducers and Converters). This is a representation of this pattern:

```elixir
connection_from_request
|> endpoint
|> router
|> custom_application
```
The custom_application can be a Phoenix controller, a Phoenix channels application, or a live view.

### Plug.Conn

Plugs == reducers, they take a Plug.Conn as he first param and returns a Plug.Conn.

## LiveView

### LiveView Flow

Router => liveview.mount/3 => liveview.render/2

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTgyNzUxNTU2MiwtMTY2MTYyODE1NywtND
c4MDE5NTgyXX0=
-->