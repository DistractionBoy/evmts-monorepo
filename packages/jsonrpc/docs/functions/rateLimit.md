[**@tevm/jsonrpc**](../README.md)

***

[@tevm/jsonrpc](../globals.md) / rateLimit

# Function: rateLimit()

> **rateLimit**(`_transport`, `__namedParameters`): `Transport`

Defined in: node\_modules/.pnpm/@ponder+utils@0.2.3\_typescript@5.8.2\_viem@2.23.10\_bufferutil@4.0.9\_typescript@5.8.2\_utf-8-validate@5.0.10\_zod@3.24.2\_/node\_modules/@ponder/utils/dist/index.d.ts:51

## Parameters

### \_transport

`Transport`

### \_\_namedParameters

#### browser?

`boolean`

#### requestsPerSecond

`number`

## Returns

`Transport`

## Description

Creates a rate limited transport that throttles request throughput.
