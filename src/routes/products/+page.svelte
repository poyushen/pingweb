<script lang="ts">
  import productImg from "../../lib/images/machine.png"
  import productImg1 from "../../lib/images/filters.png"
  import { isDrawerOpen } from "../../lib/ts/store";

  $: innerWidth = 0
</script>

<svelte:window bind:innerWidth/>
<template lang="pug">
  div.product-container
    +if("innerWidth > 1024")
      div.grid.content-end.h-full
        div.flex
          div.products.products-hover(class="w-1/2")
            a(href="/chiller")
              div.h-full.w-full.grid.content-center
                p.text-center.text-2xl Chiller
                p.text-center.text-xl Thermal Solution
              img.w-full.border(src="{productImg}" alt="product")
          div.products.products-hover(class="w-1/2")
            a(href="/filter")
              div.h-full.w-full.grid.content-center
                p.text-center.text-2xl Chemical Filter
                p.text-center.text-xl MAU, FFU, HEPA, ULPA
            img.w-full.border(src="{productImg1}" alt="product")
      +else
        div.products.mx-8.mt-12(class="{$isDrawerOpen == true ? 'products-nohover' : 'products-hover'}")
          a(href="/chiller")
            div.h-full.w-full.grid.content-center
              p.text-center.text-2xl Chiller
              p.text-center.text-xl Thermal Solution
            img.w-full.border(src="{productImg}" alt="product")
        div.products.mx-8.mt-12(class="{$isDrawerOpen == true ? 'products-nohover' : 'products-hover'}")
          a(href="/filter")
            div.h-full.w-full.grid.content-center
              p.text-center.text-2xl Chemical Filter
              p.text-center.text-xl MAU, FFU, HEPA, ULPA
          img.w-full.border(src="{productImg1}" alt="product")

</template>

<style>
  .product-container {
    height: calc(100vh - 96px);
  }

  .products {
    position: relative;
  }
  .products div {
    font-family: "futura-pt", sans-serif;
    font-weight: 500;
    font-style: normal;
    position: absolute;
    opacity: 0;
    color: black;
    z-index: 50;
  }

  .products-hover:hover img {
    opacity: 0.4;
  }
  .products-hover:hover div {
    opacity: 1;
  }

  img {
    border-color: #D98B95;
  }
</style>
