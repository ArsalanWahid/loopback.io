---
lang: en
title: 'API docs: context.context.unbind'
keywords: LoopBack 4.0, LoopBack 4
sidebar: lb4_sidebar
permalink: /doc/en/lb4/apidocs.context.context.unbind.html
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@loopback/context](./context.md) &gt; [Context](./context.context.md) &gt; [unbind](./context.context.unbind.md)

## Context.unbind() method

Unbind a binding from the context. No parent contexts will be checked.

<b>Signature:</b>

```typescript
unbind(key: BindingAddress): boolean;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  key | <code>BindingAddress</code> | Binding key |

<b>Returns:</b>

`boolean`

true if the binding key is found and removed from this context

## Remarks

If you need to unbind a binding owned by a parent context, use the code below:

```ts
const ownerCtx = ctx.getOwnerContext(key);
return ownerCtx != null && ownerCtx.unbind(key);

```

