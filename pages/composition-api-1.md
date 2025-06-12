---
clicks: 6
---

# Composition API
一种新的编写Vue的方式，组合式 API (Composition API) 是一系列 API 的集合，使我们可以使用函数而不是声明选项的方式书写 Vue 组件

<div class="grid grid-cols-2 gap-x-4">

```html {all|3,5,6,10,11,15,16,18|3-5|6-10|11-15|16-18|all} {at:0}
<script>
  export default {
    data() {
      return { count: 10 }
    },
    computed: {
      doubleCount() {
        return this.count * 2
      }
    },
    methods: {
      handleCount() {
        this.count = count.value * 2
      }
    },
    created() {
      this.handleCount()
    }
  }
</script>
```

```html {all|1,12|4|5-7|9|11|all} {at:0}
<script lang="ts" setup>
  import { ref, computed } from 'vue'

  const count = ref(10)
  const doubleCount = computed(() => {
    return count.value * 2
  })

  const handleCount = () => count.value * 2

  handleCount()
</script>
```

</div>

---
src: ./composition-api-2.md
---
