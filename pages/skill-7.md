# 技巧
可扩展性，使用 options 对象作为参数

> 在实现一个函数时,如果有选项参数的场景,通常建议使用对象来作为入参

<br>

```ts {0|1-3|5-7|all}
// good

function useScroll(element, { throttle, onScroll, ...}){...}

// bad

function useScroll(element, throttle, onScroll, ....){...}
```

<br>

<div v-click="3">

- 可以很清晰的看到两者的区别,毫无疑问第一种写法的扩展性会更强,在之后迭代中也不容易对功能本身造成一些破坏性的改动.

</div>

---
src: ./skill-8.md
---
