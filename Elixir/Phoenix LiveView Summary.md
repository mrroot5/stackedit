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
* The **router** connect a request to the module that will process it and set policies (how a request should be managed), e.x.: accept only `JSON` for `:api` requests.
* The **custom_application** can be a Phoenix controller, a Phoenix channels application, or a live view.

### Plug.Conn

Plugs == reducers, they take a Plug.Conn as he first param and returns a Plug.Conn.

## LiveView

### LiveView Flow

Router => liveview.mount/3 => liveview.render/2

### Generate a liveview

`mix phx.gen.live`

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE4ODE4NzcwMTgsLTE0NDUyNTAxNzYsLT
M4ODU1ODYyNiwxNTE4ODQzMTgsLTE2NjE2MjgxNTcsLTQ3ODAx
OTU4Ml19
-->