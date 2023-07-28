---
title: "Api Decorator"
weight: 10
date: 2023-07-26T18:59:53.878Z
showtoc: true
generated: true
---
<!-- This file was generated from the Vendure source. Do not modify. Instead, re-run the "docs:build" script -->
import MemberInfo from '@site/src/components/MemberInfo';
import GenerationInfo from '@site/src/components/GenerationInfo';
import MemberDescription from '@site/src/components/MemberDescription';


## Api

<GenerationInfo sourceFile="packages/core/src/api/decorators/api.decorator.ts" sourceLine="26" packageName="@vendure/core" />

Resolver param decorator which returns which Api the request came though.
This is useful because sometimes the same resolver will have different behaviour
depending whether it is being called from the shop API or the admin API.

Returns a string of type <a href='/reference/typescript-api/request/api-type#apitype'>ApiType</a>.

*Example*

```ts
 @Query()
 getAdministrators(@Api() apiType: ApiType) {
   if (apiType === 'admin') {
     // ...
   }
 }
```
