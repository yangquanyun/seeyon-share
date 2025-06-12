---
clicks: 3
---

<div class="grid grid-cols-2 gap-x-4">

  <div class="flex my-18 flex-col items-center text-center">
    <span class="text-6xl mb-2">🌸 Thanks</span>
    <div v-click="1" class="my-3">
      <span class="mr-2">Inspired by</span>
      <a class="mr-2 no-underline" href="https://vue.w3ctech.com" target="_blank">VueConf China</a>
      <a class="mr-2 no-underline" href="https://antfu.me/projects" target="_blank">Anthony Fu.Projects</a>
    </div>
    <div v-click="2" class="my-3">
      <span class="mr-2">Powered by</span>
      <a class="mr-2 no-underline" href="https://cn.sli.dev" target="_blank">Slidev</a>
      <a class="mr-2 no-underline" href="https://windicss.org/" target="_blank">Windi CSS</a>
      <a class="mr-2 no-underline" href="https://www.netlify.com" target="_blank">Netlify</a>
    </div>
    <div v-click="3" class="foreshow my-8">
      <div class="my-4"><b>DataForm</b> 的设计与实现</div>
      <div class="my-4"><b>Slidev</b>&<b>Netlify</b> 快速创作&部署你的WEB PPT</div>
    </div>
  </div>


  <div v-click="2">
    <div class="my-auto">
      <p>
        <a href="https://github.com/slidevjs/slidev" >
          <img src="/logo-title.png" alt="Slidev" height="300" >
        </a>
      </p>
      <div class="text-center description !-mt-8" >
        为<b>开发者</b>打造的<b>演示文稿</b>工具
      </div>
      <div class="text-center description !-mt-4" >
        <a href="https://github.com/slidevjs/slidev" class="mt-5 inline-block filter dark:invert" target="__blank">
          <img alt="GitHub stars" src="https://img.shields.io/github/stars/slidevjs/slidev?style=social">
        </a>
      </div>
    </div>
  </div>

</div>

<style>
  .slidev-layout a {
    border: none;
    color: #3AB9A4;
  }

  .foreshow {
    color: rgba(72,176,241);
  }
</style>
