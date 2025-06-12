# 技巧
响应性语法糖-->>实验性功能，默认是禁用的，需要显式选择使用

<v-click>

- ref vs. 响应式变量

</v-click>

<v-click>

> 响应式对象存在解构丢失响应性的问题，而 ref 需要到处使用 .value 则感觉很繁琐，并且在没有类型系统的帮助时很容易漏掉 .value

```ts {all|1,4|all}
let count = $ref(0)

function increment() {
  count++
}
```

</v-click>

<br/>

<v-click>

- 通过 $() 解构

</v-click>

<v-click>

> 我们常常会让一个组合函数返回一个含数个 ref 的对象，然后解构得到这些 ref。对于这种场景，响应性语法糖提供了一个 $() 宏

```ts {all|3,5|all}
import { useMouse } from '@vueuse/core'

const { x, y } = $(useMouse())

console.log(x, y)
```

</v-click>

---
src: ./model-title.md
---
