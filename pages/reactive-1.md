# 响应式
什么是响应式

<v-clicks at="1">

- Vue 最标志性的功能就是其低侵入性的响应式系统
- 相对与 React ,Vue 的响应式系统会在创建之初就建立了对数据逻辑以及视图的连接，且只会执行一次，连接直至组件销毁
- 本质上，响应性是一种可以使我们声明式地处理变化的编程范式

</v-clicks>

<div v-click class="grid grid-cols-2 gap-4">

  <div class="p-4">
    <h3 class="pt-5">Excel 中的公式</h3>
    <SpreadSheet v-click class="mt-4"/>
  </div>

  <div class="p-26 text-xs leading-6">
    这里单元格 A2 中的值是通过公式 = A0 + A1 来定义的 (你可以在 A2 上点击来查看或编辑该公式)，因此最终得到的值为 3，正如所料。但如果你试着更改 A0 或 A1，你会注意到 A2 也随即自动更新了。
  </div>
</div>

---
src: ./skill-title.md
---
