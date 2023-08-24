<template>
  <div py4>
    <div flex justify-between items-center>
      <div mr-20>Tools</div>
      <div flex items-center gap-4>
        <div class="w-max py-4 px-10 rounded-sm bg-[#487DCF]">Axe DevTools</div>
        <div class="w-max py-4 px-10 rounded-sm bg-[#487DCF]">Screen reader</div>
      </div>
    </div>
    <hr my-10>
    <div flex justify-between items-center>
      <div mr-20>Standards</div>
      <div flex items-center gap-4>
        <div class="w-max py-4 px-4 rounded-sm bg-[#487DCF] flex-all-center flex-col">
          <p>WCAG</p>
          <p class="text-12px">Web Content Accessibility Guidelines</p>
        </div>
        
        <div class="w-max py-4 px-4 rounded-sm bg-[#487DCF] flex-all-center flex-col">
          <p>ARIA</p>
          <p class="text-12px">Accessible Rich Internet Applications</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
p{
  margin: 0 !important;
}
.box {
  --at-apply: 'flex items-center gap-4 px2 py4 rounded-5px transition-all duration-600 rounded !hover:op100 group-hover:op50';
}
</style>
