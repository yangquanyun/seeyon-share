---
clicks: 4
---

# 技巧
`ref` 构成的对象

```html {all|4-9|11|12-15|all} {at: 0}
<script setup lang="ts">
import { ref, reactive } from 'vue'

function useUserInfo() {
  return {
    name: ref('老六'),
    age: ref(66)
  }
}

const { name, age } = useUserInfo()
const user = reactive(useUserInfo())

user.name === name.value // true
user.age === age.value // true
</script>
```

<div v-click="2">

  > 使用 ES6 解构对象，保持响应

  </div>

  <div class="my-2" v-click="3">

  > 使用 `reactive` 将其转换为对象，自动解包

</div>

---
src: ./skill-6.md
---
