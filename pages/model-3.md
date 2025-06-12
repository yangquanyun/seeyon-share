---
clicks: 8
---

# 模式
数据驱动

> 泛前端领域，模型驱动视图已经是一个很老的话题。数据驱动能帮我们快速的去搭建通用型视图，所以，数据驱动的可配置性尤为重要。

<div class="grid grid-cols-2 gap-x-4">

```ts {0|all|all|0|0|4|1,5|1,5|all} {at: 0}
// state
export function useFormState() {
  const preFormState = reactive({
    formModel: {},
    formSchema: [],
  });
  return { formState };
}





// -->
```

```ts {0|all|0|all|0|0|1,3-12|1,3-12|all} {at: 0}
// logic
export function useformLogic() {
  const getFormSchema = () => {
    {
      prop: 'name',
      component: DATA_FORM_COMPONENT.CF_INPUT,
      label: '姓名',
      required: true,
      componentAttrs: {},
      afterSlots: [],
    }
  }
  return { getFormSchema }
}
```

</div>

```html {0|all|0|0|all|3|0|3|all} {at: 0}
<!-- view -->
<template>
  <DataForm v-model="formState.formModel" :schema="formState.formSchema"/>
</template>
```

---
src: ./model-4.md
---
