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



### Context

A Phoenix Context is a module in your Phoenix application that provides an API for a service or resource.
It is responsible for managing uncertainty, external interfaces, and process machinery.

## LiveView

### LiveView Flow

Router => liveview.mount/3 => liveview.render/2

### Generate a LiveView

We’ll construct the generator command such that it will generate a Catalog context with a schema for Product, corresponding to a products database table. A product will have name , description , unit_price , and SKU fields, like this:

```bash
mix phx.gen.live Catalog Product products name:string description:string unit_price:float sku:integer:unique
```




#### Context (boundary / api part)



> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbOTU1Mzk3Mjg0LDE5NTA0NDMxNjAsNzgwND
M3NTM0LC05ODg1ODE0ODQsLTE4ODE4NzcwMTgsLTE0NDUyNTAx
NzYsLTM4ODU1ODYyNiwxNTE4ODQzMTgsLTE2NjE2MjgxNTcsLT
Q3ODAxOTU4Ml19
-->