<script lang="ts">
  import filterNav1 from "../../lib/images/filter1.png"
  import filterNav2 from "../../lib/images/filter2.png"

  $: innerWidth = 0
</script>

<svelte:window bind:innerWidth/>
<template lang="pug">
  .chiller-container.px-24
    +if("innerWidth > 1024")
      div.w-full.mt-8.flex
        img.h-96(src="{filterNav1}")(style="opacity: 0.8")(class="w-1/2")
        img.h-96(src="{filterNav2}")(style="opacity: 0.8")(class="w-1/2")
      +elseif("innerWidth > 768")
        div.w-full.mt-8.flex
          img.h-64(src="{filterNav1}")(style="opacity: 0.8")(class="w-1/2")
          img.h-64(src="{filterNav2}")(style="opacity: 0.8")(class="w-1/2")
        +else
          div.w-full
            img.w-96.h-48(src="{filterNav1}")(style="opacity: 0.8")
            img.w-96.h-48.mt-2(src="{filterNav2}")(style="opacity: 0.8")
    +if("innerWidth > 1024")
      div.grid.grid-cols-2.mt-8
        div
          p.text-xl Client:
          div.mt-4
            u Taiwan
            div
              p TSMC/UMC/ASE/HanStar/NTC
          div.mt-4
            u.mt-8 China
            div
              p TSMC China/CXMT/NEXCHIP/BOE/Spil/Amkor/
              p Avary Holding/JHIC/Nata/CR Micro/UniMos/
              p Sanan IC/SJ Semi/CanSemi/Yangtze Memory/XMC
        div.mb-8
          p.text-xl &nbsp
          p.mt-6 - ISO 900, FM4920, UL-900, 高新技術證書
          p.mt-4 - 半導體電子級, 空調系統, 醫院, 製藥業, 核能發電廠, 實驗室, 軍方, 生化科技
          p.mt-4 - 40+ services in the field conform clean air requirements. To be the leader in air filter. (MAU, FFU)
          p.mt-4 - AMC control: 2nm. 客製化控管條件及最佳濾材調配, 最優化控管汙染分子
          p.mt-4 - Recycle 資源再利用: 靈活配合設備框材尺寸及材料. 框材回收再利用. 落實高效節約生產成本及減少廢棄物處理. 打造低碳排& Environmental
          p.mt-4 - 先進檢測設備, 落實原物料分析,品質穩定控管. 台灣工研院, 日本住友化學, 實驗室 (ISO10121-2 GPACD, 测試標氣, 離子層析色譜儀, 台灣工研院化學濾材测試設備, 全尺寸濾網壓損測試設備). EN1822, ASHRAE 52.1-1992, EN779
          p.mt-4 - 全球領先工藝-熱溶. Avoid outgassing & 電力耗損
      +else
        div
          p.text-xl.mt-8 Client:
          div.mt-4
            u Taiwan
            div
              p TSMC/UMC/ASE/HanStar/NTC
          div.mt-4
            u.mt-8 China
            div
              p TSMC China/CXMT/NEXCHIP/BOE/Spil/Amkor/
              p Avary Holding/JHIC/Nata/CR Micro/UniMos/
              p Sanan IC/SJ Semi/CanSemi/Yangtze Memory/XMC
        div.mb-8.mt-8
          p.text-xl Information
          p.mt-4 - ISO 900, FM4920, UL-900, 高新技術證書
          p.mt-4 - 半導體電子級, 空調系統, 醫院, 製藥業, 核能發電廠, 實驗室, 軍方, 生化科技
          p.mt-4 - 40+ services in the field conform clean air requirements. To be the leader in air filter. (MAU, FFU)
          p.mt-4 - AMC control: 2nm. 客製化控管條件及最佳濾材調配, 最優化控管汙染分子
          p.mt-4 - Recycle 資源再利用: 靈活配合設備框材尺寸及材料. 框材回收再利用. 落實高效節約生產成本及減少廢棄物處理. 打造低碳排& Environmental
          p.mt-4 - 先進檢測設備, 落實原物料分析,品質穩定控管. 台灣工研院, 日本住友化學, 實驗室 (ISO10121-2 GPACD, 测試標氣, 離子層析色譜儀, 台灣工研院化學濾材测試設備, 全尺寸濾網壓損測試設備). EN1822, ASHRAE 52.1-1992, EN779
          p.mt-4 - 全球領先工藝-熱溶. Avoid outgassing & 電力耗損

</template>

<style>
  p, u {
    font-family: "futura-pt", sans-serif;
    font-weight: 500;
    font-style: normal;
  }
</style>
