<script lang="ts">
  import semiconductor from "../../lib/images/semiconductor.jpg"

  $:outerWidth = 0;
</script>

<svelte:window bind:outerWidth />
<template lang="pug">
  div.profile-container(class="mx-8 lg:mx-48")
    +if("outerWidth > 1024")
      div.mt-48.grid.grid-cols-2
        div.profile-main.content-center
          p.text-2xl "Total solution is the core principle in Echotrade, which is making never end & bigger partnership in semiconductor. Innovation with new technology creativity , strong & professional supply chain & trusted. it wasn’t a challenge to be taken lightly."
        img.p-4(src="{semiconductor}" alt="semicondustor" style="opacity: 0.8")
      +else
        img.mt-12(class="lg:p-4" src="{semiconductor}" alt="semiconductor" style="opacity: 0.8")
        div.profile-main.content-center
          p.text-2xl.mt-8 "Total solution is the core principle in Echotrade, which is making never end & bigger partnership in semiconductor. Innovation with new technology creativity , strong & professional supply chain & trusted. it wasn’t a challenge to be taken lightly."
    div.profile-sub.mt-16.grid.justify-items-end.w-full
      div(class="w-full lg:w-8/12")
        div.my-4
          p.text-xl Innovation
          p.textGray.text-base As a semiconductor, we are a pioneer in technology, a collective of professional R&D design and experience. We use creativity and originality to drive new forms of innovation based on a deep understanding of customer needed
        div.my-4
          p.text-xl Global Creativity
          p.textGray.text-base With an in-house center of R&D and industry talent from around the world, It leverage our diversity and unique patents to service our customers and protect global environment through resource substitution and recycling.
        div.my-4
          p.text-xl Trusted
          p.textGray.text-base We integrate the three areas of raw materials, design and production into one, ensuring the quality consistency and stability of all products, and providing top quality, high efficiency of performance & knowledge in the field, that with an impressive and powerful.
</template>

<style>
  .profile-container {
    height: calc(100vh - 96px);
  }
  .profile-main p {
    font-family: "futura-pt", sans-serif;
    font-weight: 500;
    font-style: normal;
    color: #393D3F;
    line-height: 45px;
  }

  .textGray {
    color: #7B7B7B;
    line-height: 30px;
    font-family: "futura-pt", sans-serif;
    font-weight: 400;
    font-style: normal;
  }
</style>
