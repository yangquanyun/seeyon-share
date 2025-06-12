---
clicks: 5
---

# Composition API
更好的逻辑复用，清晰的上下文提示

<div>

```ts {all|6-10|all} {at:0}
// hooks

import { computed, ref } from 'vue';

export function useDoubleCount() {
  const count = ref(0);
  const doubleCount = computed(() => count.value * 2);
  const handleCount = () => count.value * 2;

  return { count, doubleCount, handleCount };
}
```

</div>

<div class="grid grid-cols-2 gap-x-4">

```html {0|0|0|1-4,8|1-4,8|all} {at:0}
<!-- page A -->

<script lang="ts" setup>
  import { useDoubleCount } from './hooks'
  const {
    count, doubleCount, handleCount
  } = useDoubleCount()
</script>
```

```html {0|0|0|0|1-4,8|all} {at:0}
<!-- page B -->

<script lang="ts" setup>
  import { useDoubleCount } from './hooks'
  const {
    count, doubleCount, handleCount
  } = useDoubleCount()
</script>
```

</div>

---
src: ./composition-api-4.md
---
