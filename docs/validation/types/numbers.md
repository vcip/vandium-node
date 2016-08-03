# Numbers

Number validators can be created by calling `vandium.types.number()`. The implementation is based on `Joi` and thus can use functionality
available in the `Joi` library for the `number` type.

Numbers can be validated against ranges and forced to be integers:

```js
{
	age: vandium.types.number().integer().min( 0 ).max( 130 ).required()
}
```

To specify the number of decimal places allowed:

```js
{
	price: vandium.types.number(). precision( 2 ).required()
}
```

For more information on how to configure numbers, see the [joi numbers reference](https://github.com/hapijs/joi/tree/v8.0.5#number).