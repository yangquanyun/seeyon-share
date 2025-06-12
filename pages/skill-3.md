# 技巧
VueUse `useVModel`

<div class="grid grid-cols-2 gap-x-4"><div>

# v-model

```html {monaco} {height: '255px'}
<script lang="ts" setup>
  const props = defineProps<{
    modelValue: string
  }>()
  const emit = defineEmits(['update:modelValue']);

  const data = computed({
    get() {
      return props.modelValue;
    },
    set(val) {
      emit('update:modelValue', val);
    },
  });
</script>
```

<div class="mt-4" v-click>

- 需要在组件内写冗余的代码

</div>

</div><div>

# useVModel

```html {monaco} {height: '255px'}
<script lang="ts" setup>
  import { useVModel } from '@vueuse/core'

  const props = defineProps<{
    modelValue: string
  }>()
  const emit = defineEmits(['update:modelValue'])

  // const data = useVModel(props, 'modelValue', emit)
</script>
```

<div class="mt-4" v-click>

- 直接将 `useVModel` 返回的数据作为响应式对象用即可

</div>
</div></div>

---
src: ./skill-4.md
---
