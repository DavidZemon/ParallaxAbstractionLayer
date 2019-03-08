Language Agnostic API
=====================

Syntax
------

`<function_name>(<type> <parameterName>[, <type> <parameterName>...]) : <return type>[, <return type>] ! <error scenario>[, <error scenario>]`

### Types

* `void` (return values only)
* `boolean`
* `number`
* `string`
* `list<type>`
* `map<key type, value type>`
* `object type`

### Example

`start_pwm(number pin, number frequency, number duty) : void ! InvalidArgument`


