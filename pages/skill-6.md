# 技巧
副作用清除

> Vue 中 `watch` 和 `computed` API 会在组件销毁时自动解除其内部的依赖监听。<br>
> 我们在写自定义函数的时候也应该遵循同样的模式。

<br>

<div class="grid grid-cols-2 gap-x-4">

<div v-click>

- 组件销毁时清除

```html {monaco} {height: '290px'}
<script setup lang="ts">
import { onUnmounted } from 'vue'

export function useEventListener(target: EventTarget, name: string, fn: any) {
  target.addEventListener(name, fn)

  onUnmounted(() => {
    // target.removeEventListener(name, fn)
  })
}
</script>
```

</div>

<div v-click>

- 自动捕获副作用，批量清除

```html {monaco} {height: '290px'}
<script setup lang="ts">
const scope = effectScope()

scope.run(() => {
  const doubled = computed(() => counter.value * 2)

  watch(doubled, () => console.log(doubled.value))

  watchEffect(() => console.log('Count: ', doubled.value))
})

// 处理掉当前作用域内的所有 effect
// scope.stop()
</script>
```

</div>

</div>

---
src: ./skill-7.md
---
