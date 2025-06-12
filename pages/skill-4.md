# 技巧
VueUse `useEventListener`

- 轻松使用 EventListener,在挂载时使用 addEventListener 注册，在卸载时自动删除事件监听器

<v-click>

```ts
import { useEventListener } from '@vueuse/core'
useEventListener(document, 'visibilitychange', (evt) => { console.log(evt) })
```

</v-click>

<v-click>

<br/>

- 可以传递一个 ref 作为事件目标，使用EventListener将取消注册之前的事件并在你更改目标时注册新的事件

</v-click>

<v-click>

```ts {all|2|all}
import { useEventListener } from '@vueuse/core'
const element = ref<HTMLDivElement>()
useEventListener(element, 'keydown', (e) => { console.log(e.key) })
```

```html
<div v-if="cond" ref="element">Div1</div>
<div v-else ref="element">Div2</div>
```

</v-click>

<v-click>

<br/>

- 还可以调用返回的来注销监听器。

</v-click>

<v-click>

```ts {all|2|3|all}
import { useEventListener } from '@vueuse/core'
const cleanup = useEventListener(document, 'keydown', (e) => { console.log(e.key) })
cleanup() // This will unregister the listener.
```

</v-click>

---
src: ./skill-5.md
---
