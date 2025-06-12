---
clicks: 7
---

# 可组合的函数
什么是可组合的函数

<v-clicks>

- 可组合的函数简单来说就是函数间可以建立组合关系
- 组合式函数约定用驼峰命名法命名，并以“use”作为开头

</v-clicks>

<div v-if="Number($slidev.nav.route.query.clicks) > 2" class="grid grid-cols-2 gap-x-4">

```ts {all|all|all|all|4-8|4-8|10-12|all} {at: 0}
export function useInitForm({
  preFormState, basicFormState, customFormState
}) {
  const { getPreFormSchema } = usePreFormLogic(preFormState);

  const { getBasicFormSchema } = useBasicFormLogic(basicFormState);

  const { getCustomFormSchema } = useCustomFormLogic(customFormState);

  const initForm = () => {
    // composable logic
  }
  return { initForm }
}
```

<div>
  <span v-click="3">

  - `useInitForm` 的实现组合了三个函数,将一个个单一职责的函数组合形成另一个函数,达到逻辑复用的能力

  </span>

  <span  v-click="5">

  - 当然,每个函数也都可以进行独立使用,我们可以根据自己的需要进行选择

  </span>

  <span  v-click="6">

  - 我们在处理功能函数的时候可以做到更好的关注点分离,比如处理 `useInitForm` 时我们只需要关注不同表单功能的实现,并不需要关注具体表单内部的逻辑与实现

  </span>

</div>

</div>

---
src: ./composition-api-5.md
---
