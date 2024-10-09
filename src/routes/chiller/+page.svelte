<script lang="ts">
  import chillerNav from "../../lib/images/banner.png"
</script>

<template lang="pug">
  .chiller-container.px-24
    div.w-full.mt-8
      img(src="{chillerNav}")(style="opacity: 0.8")
    div.grid.grid-cols-2.mt-8
      div
        p.text-xl Client:
        div.mt-4
          u Taiwan
          div
            p TSMC/UMC/VIS/Powerchip/Innolux/
            p Winbond/Maxchip/Xintec/Applied Material
        div.mt-4
          u.mt-8 China
          div
            p CXMT/HUAWEI/TSMC China/CRC/HJTC/SMIC/NEXCHIP
      div.mb-8
        p.text-xl &nbsp
        p.mt-6 - ISO 9001: 1015/CNS12681
        p.mt-4 - Reliable & precision of temperature control & solutions
        p.mt-4 - 20+ years experience, design ability with high integration of controllers base on customized
        p.mt-4 - Especial heat exchange design& technology to achieve electrify saving, in order to meet global Environmental

</template>

<style>
  p, u {
    font-family: "futura-pt", sans-serif;
    font-weight: 500;
    font-style: normal;
  }
</style>
