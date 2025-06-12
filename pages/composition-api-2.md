---
clicks: 7
---

# Composition API
 

<div class="grid grid-cols-2 gap-x-4 gap-y-4">

###### Option API 存在的问题

###### Composition API 提供的能力

<v-clicks at="1">

- 复用困难
- 上下文丢失
- 有限的TypeScript支持
- 基于 Option API 组织代码

</v-clicks>

<v-clicks at="1">

- 极易复用（本质就是 JavaScript 代码）
- 更好的上下文支持
- 强大的 TypeScript 支持
- 按功能、类型组织代码

</v-clicks>

</div>

<div class="my-12" v-if="$slidev.nav.route.query.clicks !== '7'" v-click="6">

> 组合式 API 不像选项式 API 那样会手把手教你该把代码放在哪里。<br>
> 但反过来，它却让你可以像编写普通的 JavaScript 那样来编写组件代码。<br>
> 这意味着你能够，并且应该在写组合式 API 的代码时也运用上所有普通 JavaScript 代码组织的最佳实践。<br>
> 如果你可以编写组织良好的 JavaScript，你也应该有能力编写组织良好的组合式 API 代码。

</div>

<div class="my-12" v-click="7">

> 相对于 React Hooks ，Vue 仅调用 setup() 或 `<script setup>` 的代码一次。这使得代码更符合日常 JavaScript 的直觉，不需要担心闭包变量的问题。组合式 API 也并不限制调用顺序，还可以有条件地进行调用。<br>
> Vue 的响应性系统运行时会自动收集计算属性和侦听器的依赖，因此无需手动声明依赖。<br>
> 无需手动缓存回调函数来避免不必要的组件更新。Vue 细粒度的响应性系统能够确保在绝大部分情况下组件仅执行必要的更新。对 Vue 开发者来说几乎不怎么需要对子组件更新进行手动优化。

</div>

---
src: ./composition-api-3.md
---
