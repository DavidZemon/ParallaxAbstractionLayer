Language Agnostic API
=====================

Syntax
------

### Types

* `void` (return values only)
* `boolean`
* `number`
* `string`
* `list<type>`
* `map<key type, value type>`
* `object type`

### Function & Methods

`<function_name>(<type> <parameterName>[, <type> <parameterName>...]) : <return type>[, <return type>] ! <error scenario>[, <error scenario>]`

#### Example

`pin(number pin, boolean value) : void ! InvalidPinNumber`

### Objects

Note that, for simplicity, only `public` and `private` will be used in this API.
It will be up to the specific language designers to choose whether a "private"
property should be implemented as `private`, `protected`, `package-protected`,
etc.

Constructor/destructor methods should be named `constructor` and `destructor`,
can not be static, and do not have return types. They are otherwise identical to
other object methods.

```
<ObjectName>:
  public:
    [<static>] <public method or field>
    
  private:
    [<static>] <non-public method or field>
```

#### Example

```
UartTx:
  public:
    constructor(number pin, number baudRate) ! InvalidPinNumber, InvalidBaudRate
    
    send(list<number> bytes) : void
```
