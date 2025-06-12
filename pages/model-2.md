---
clicks: 5
---

# 模式
状态共享 ->> 局部作用域下状态共享

> 得益于 Composition API 的灵活性且可以独立于组件外运行 <br>
> 相对独立的业务模块可以很方便的使用`reactive` `ref`来做状态共享


<div class="grid grid-cols-2 gap-x-4">

```ts {0|1,3-6|0|0|0} {at: 0}
// state.ts global
import { reactive } from 'vue'

export const state = reactive({
  count: 0
})


// -->
```

```ts {0|1,4-9|1,4-9|1,4-9|all} {at: 0}
// state.ts local
import { reactive } from 'vue'

const useState = () => {
  const state = reactive({
    count: 0
  })
  return { state }
}

```

</div>

<div class="grid grid-cols-2 gap-x-4">

```html {0|0|1,3,4|1,3,4|1,7|all} {at: 0}
<!-- ComponentA.vue -->
<script setup>
import { useState } from './state.ts'
const { state } = useState()
</script>

<template>From A: {{ state.count }}</template>
```

```html {0|0|0|1,3,4|1,7|all} {at: 0}
<!-- ComponentB.vue -->
<script setup>
import { useState } from './state.ts'
const { state } = useState()
</script>

<template>From B: {{ state.count }}</template>
```

</div>

---
src: ./model-3.md
---
