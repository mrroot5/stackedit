# Phoenix LiveView

A summary for Phoenix and Phoenix LiveView.

## Phoenix

### Flow CRC pattern

Phoenix follows the pattern **CRC** (Constructors Reducers and Converters). This is a representation of this pattern:

```elixir
connection_from_request
|> endpoint
|> router
|> custom_application
```
* The **endpoint** has a couple of configurations and Plug where the router is the last one.
* The **router** is 
* The **custom_application** can be a Phoenix controller, a Phoenix channels application, or a live view.

### Plug.Conn

Plugs == reducers, they take a Plug.Conn as he first param and returns a Plug.Conn.

## LiveView

### LiveView Flow

Router => liveview.mount/3 => liveview.render/2

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTM4ODU1ODYyNiwxNTE4ODQzMTgsLTE2Nj
E2MjgxNTcsLTQ3ODAxOTU4Ml19
-->