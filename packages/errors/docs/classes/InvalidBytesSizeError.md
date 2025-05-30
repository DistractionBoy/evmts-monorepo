[**@tevm/errors**](../README.md)

***

[@tevm/errors](../globals.md) / InvalidBytesSizeError

# Class: InvalidBytesSizeError

Defined in: [packages/errors/src/data/InvalidByteSizeError.js:43](https://github.com/evmts/tevm-monorepo/blob/main/packages/errors/src/data/InvalidByteSizeError.js#L43)

Represents an error that occurs when the size of the bytes does not match the expected size.

## Example

```javascript
import { InvalidBytesSizeError } from '@tevm/errors'
import { hexToBytes } from '@tevm/utils'

function requireBytes32(value) {
  const bytes = hexToBytes(value)
  if (bytes.length !== 32) {
    throw new InvalidBytesSizeError(bytes.length, 32)
  }
  return bytes
}

try {
  requireBytes32('0x1234') // This will throw an InvalidBytesSizeError
} catch (error) {
  if (error instanceof InvalidBytesSizeError) {
    console.error(`Invalid bytes size: ${error.message}`)
    console.log(`Actual size: ${error.size}, Expected size: ${error.expectedSize}`)
  }
}
```

## Extends

- [`InternalError`](InternalError.md)

## Constructors

### new InvalidBytesSizeError()

> **new InvalidBytesSizeError**(`size`, `expectedSize`, `message`?, `args`?): [`InvalidBytesSizeError`](InvalidBytesSizeError.md)

Defined in: [packages/errors/src/data/InvalidByteSizeError.js:64](https://github.com/evmts/tevm-monorepo/blob/main/packages/errors/src/data/InvalidByteSizeError.js#L64)

Constructs an InvalidBytesSizeError.

#### Parameters

##### size

`number`

The actual size of the bytes.

##### expectedSize

`number`

The expected size of the bytes.

##### message?

`string`

Human-readable error message.

##### args?

[`InvalidBytesSizeErrorParameters`](../interfaces/InvalidBytesSizeErrorParameters.md) = `{}`

Additional parameters for the error.

#### Returns

[`InvalidBytesSizeError`](InvalidBytesSizeError.md)

#### Overrides

[`InternalError`](InternalError.md).[`constructor`](InternalError.md#constructors)

## Properties

### \_tag

> **\_tag**: `string`

Defined in: [packages/errors/src/data/InvalidByteSizeError.js:78](https://github.com/evmts/tevm-monorepo/blob/main/packages/errors/src/data/InvalidByteSizeError.js#L78)

Same as name, used internally.

#### Inherited from

[`InternalError`](InternalError.md).[`_tag`](InternalError.md#_tag)

***

### cause

> **cause**: `any`

Defined in: [packages/errors/src/ethereum/BaseError.js:114](https://github.com/evmts/tevm-monorepo/blob/main/packages/errors/src/ethereum/BaseError.js#L114)

#### Inherited from

[`InternalError`](InternalError.md).[`cause`](InternalError.md#cause)

***

### code

> **code**: `number`

Defined in: [packages/errors/src/ethereum/BaseError.js:112](https://github.com/evmts/tevm-monorepo/blob/main/packages/errors/src/ethereum/BaseError.js#L112)

#### Inherited from

[`InternalError`](InternalError.md).[`code`](InternalError.md#code)

***

### details

> **details**: `string`

Defined in: [packages/errors/src/ethereum/BaseError.js:91](https://github.com/evmts/tevm-monorepo/blob/main/packages/errors/src/ethereum/BaseError.js#L91)

#### Inherited from

[`InternalError`](InternalError.md).[`details`](InternalError.md#details)

***

### docsPath

> **docsPath**: `undefined` \| `string`

Defined in: [packages/errors/src/ethereum/BaseError.js:96](https://github.com/evmts/tevm-monorepo/blob/main/packages/errors/src/ethereum/BaseError.js#L96)

#### Inherited from

[`InternalError`](InternalError.md).[`docsPath`](InternalError.md#docspath)

***

### expectedSize

> **expectedSize**: `number`

Defined in: [packages/errors/src/data/InvalidByteSizeError.js:54](https://github.com/evmts/tevm-monorepo/blob/main/packages/errors/src/data/InvalidByteSizeError.js#L54)

The expected size of the bytes.

***

### message

> **message**: `string`

Defined in: node\_modules/.pnpm/typescript@5.8.2/node\_modules/typescript/lib/lib.es5.d.ts:1077

Human-readable error message.

#### Inherited from

[`InternalError`](InternalError.md).[`message`](InternalError.md#message-1)

***

### meta

> **meta**: `undefined` \| `object`

Defined in: [packages/errors/src/ethereum/InternalErrorError.js:75](https://github.com/evmts/tevm-monorepo/blob/main/packages/errors/src/ethereum/InternalErrorError.js#L75)

Optional object containing additional information about the error.

#### Inherited from

[`InternalError`](InternalError.md).[`meta`](InternalError.md#meta)

***

### metaMessages

> **metaMessages**: `undefined` \| `string`[]

Defined in: [packages/errors/src/ethereum/BaseError.js:100](https://github.com/evmts/tevm-monorepo/blob/main/packages/errors/src/ethereum/BaseError.js#L100)

#### Inherited from

[`InternalError`](InternalError.md).[`metaMessages`](InternalError.md#metamessages)

***

### name

> **name**: `string`

Defined in: [packages/errors/src/data/InvalidByteSizeError.js:77](https://github.com/evmts/tevm-monorepo/blob/main/packages/errors/src/data/InvalidByteSizeError.js#L77)

The name of the error, used to discriminate errors.

#### Inherited from

[`InternalError`](InternalError.md).[`name`](InternalError.md#name)

***

### shortMessage

> **shortMessage**: `string`

Defined in: [packages/errors/src/ethereum/BaseError.js:104](https://github.com/evmts/tevm-monorepo/blob/main/packages/errors/src/ethereum/BaseError.js#L104)

#### Inherited from

[`InternalError`](InternalError.md).[`shortMessage`](InternalError.md#shortmessage)

***

### size

> **size**: `number`

Defined in: [packages/errors/src/data/InvalidByteSizeError.js:48](https://github.com/evmts/tevm-monorepo/blob/main/packages/errors/src/data/InvalidByteSizeError.js#L48)

The actual size of the bytes.

***

### stack?

> `optional` **stack**: `string`

Defined in: node\_modules/.pnpm/typescript@5.8.2/node\_modules/typescript/lib/lib.es5.d.ts:1078

#### Inherited from

[`InternalError`](InternalError.md).[`stack`](InternalError.md#stack)

***

### version

> **version**: `string`

Defined in: [packages/errors/src/ethereum/BaseError.js:108](https://github.com/evmts/tevm-monorepo/blob/main/packages/errors/src/ethereum/BaseError.js#L108)

#### Inherited from

[`InternalError`](InternalError.md).[`version`](InternalError.md#version)

***

### code

> `static` **code**: `number` = `-32603`

Defined in: [packages/errors/src/ethereum/InternalErrorError.js:52](https://github.com/evmts/tevm-monorepo/blob/main/packages/errors/src/ethereum/InternalErrorError.js#L52)

The error code for InternalError.

#### Inherited from

[`InternalError`](InternalError.md).[`code`](InternalError.md#code-1)

***

### prepareStackTrace()?

> `static` `optional` **prepareStackTrace**: (`err`, `stackTraces`) => `any`

Defined in: node\_modules/.pnpm/@types+node@22.13.10/node\_modules/@types/node/globals.d.ts:143

Optional override for formatting stack traces

#### Parameters

##### err

`Error`

##### stackTraces

`CallSite`[]

#### Returns

`any`

#### See

https://v8.dev/docs/stack-trace-api#customizing-stack-traces

#### Inherited from

[`InternalError`](InternalError.md).[`prepareStackTrace`](InternalError.md#preparestacktrace)

***

### stackTraceLimit

> `static` **stackTraceLimit**: `number`

Defined in: node\_modules/.pnpm/@types+node@22.13.10/node\_modules/@types/node/globals.d.ts:145

#### Inherited from

[`InternalError`](InternalError.md).[`stackTraceLimit`](InternalError.md#stacktracelimit)

## Methods

### walk()

> **walk**(`fn`?): `unknown`

Defined in: [packages/errors/src/ethereum/BaseError.js:137](https://github.com/evmts/tevm-monorepo/blob/main/packages/errors/src/ethereum/BaseError.js#L137)

Walks through the error chain.

#### Parameters

##### fn?

`Function`

A function to execute on each error in the chain.

#### Returns

`unknown`

The first error that matches the function, or the original error.

#### Inherited from

[`InternalError`](InternalError.md).[`walk`](InternalError.md#walk)

***

### captureStackTrace()

#### Call Signature

> `static` **captureStackTrace**(`targetObject`, `constructorOpt`?): `void`

Defined in: node\_modules/.pnpm/@types+node@22.13.10/node\_modules/@types/node/globals.d.ts:136

Create .stack property on a target object

##### Parameters

###### targetObject

`object`

###### constructorOpt?

`Function`

##### Returns

`void`

##### Inherited from

[`InternalError`](InternalError.md).[`captureStackTrace`](InternalError.md#capturestacktrace)

#### Call Signature

> `static` **captureStackTrace**(`targetObject`, `constructorOpt`?): `void`

Defined in: node\_modules/.pnpm/bun-types@1.2.5/node\_modules/bun-types/globals.d.ts:1441

Create .stack property on a target object

##### Parameters

###### targetObject

`object`

###### constructorOpt?

`Function`

##### Returns

`void`

##### Inherited from

[`InternalError`](InternalError.md).[`captureStackTrace`](InternalError.md#capturestacktrace)
