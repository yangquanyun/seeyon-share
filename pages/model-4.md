---
clicks: 10
---

# 模式
积木式编程

> 现有的普遍开发模式对于复杂的业务场景往往使得开发繁琐且复杂，整个工程也大量存在难以维护的代码<br>
> 那 Composable Vue 可以让我们像玩乐高一样 `简单` `快乐` 的编程

<div class="grid grid-cols-2 gap-x-4">

<div>

```ts {0|all|1-3|5-8|9-12|8,12|7,11|0|0|all} {at: 0}
├── components // 视图层
│   ├── DataFormSchema
│   └── DrawerContent.vue
├── composables
│   ├── logic  // 逻辑层
│   │   ├── index.ts
│   │   ├── useBasicFormLogic.ts
│   │   ├── usePreFormLogic.ts
│   ├── state  // 模型层
│   │   ├── index.ts
│   │   ├── useBasicFormState.ts
│   │   ├── usePreFormState.ts
│   └── types
│       └── index.ts
└── index.vue
```

<div v-click="10" class="">
  <a class="no-underline" href="https://git.dustess.com/dustess-f2e/crm-groups/scrm-manage-salechance/-/tree/master-yangqy/src/components/add-or-edit-sale-chance-new" target="_blank">在业务场景中的具体实践</a>
  <a class="no-underline" href="https://vscode.dev/github/Muzlin/talks" target="_blank">
    <ri-github-line class="opacity-50 ml-3 color"/>
  </a>
</div>

</div>

```html {0|0|0|0|0|2,3|4,5|6-11|13-16|all} {at: 0}
<script lang="ts" setup>
const { preFormState } = usePreFormState();
const { getPreFormSchema } = usePreFormLogic(preFormState);
const { basicFormState } = useBasicFormState();
const { getBasicFormSchema } = useBasicFormLogic(basicFormState);

// 生成表单 schema
const generateFormSchema = () => {
  getPreFormSchema()
  getBasicFormSchema()
};

function execSetup() {
  generateFormSchema()
  // ...other logic
}
</script>
```

</div>

<style>
  .slidev-layout a, .color {
    border: none;
    color: #3AB9A4;
  }
</style>

---
src: ./think-title.md
---
