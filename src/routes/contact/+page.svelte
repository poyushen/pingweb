<script lang="ts">
  import addressIcon from "../../lib/images/pin.png"
  import phoneIcon from "../../lib/images/phone-call.png"
  import mailIcon from "../../lib/images/mail.png"
  import invoiceIcon from "../../lib/images/file.png"

  $:innerWidth = 0;
</script>

<svelte:window bind:innerWidth />
<template lang="pug">
  +if("innerWidth > 1024")
    div.contact-container.content-end
      div.mx-48.mt-12.grid.grid-cols-2(class="h-4/12")
        div
          p.text-lg PING HUANG
          div.h-6.flex.mt-2
            img.h-full.p-1(src="{mailIcon}" alt="mail")
            p.ml-2 Ping_huang@ecotrade.com.tw
        div
          div.h-6.flex
            img.h-full.p-1(src="{addressIcon}" alt="address")
            p.ml-2 高雄市苓雅區四維三路57巷37號9樓之4
          div.h-6.flex.mt-2
            img.h-full.p-1(src="{phoneIcon}" alt="phone")
            p.ml-2 +886 972322333
      div.mx-48.mt-12.mb-8(class="h-8/12")
        iframe.w-full.h-96(src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3682.95978328861!2d120.30820457549315!3d22.617976931305407!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x346e049c94bb90a7%3A0xfeb56573d9c9549c!2zODAy6auY6ZuE5biC6IuT6ZuF5Y2A5Zub57at5LiJ6LevNTflt7czN-iZnw!5e0!3m2!1szh-TW!2stw!4v1728062840137!5m2!1szh-TW!2stw" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade")
    +else
      div.contact-container.mt-8
        div.mx-12.mt-4
          p.text-lg PING HUANG
          div.h-6.flex.mt-2
            img.h-full.p-1(src="{mailIcon}" alt="mail")
            p.ml-2 Ping_huang@ecotrade.com.tw
          div.h-6.flex.mt-2
            img.h-full.p-1(src="{addressIcon}" alt="address")
            p.ml-2 高雄市苓雅區四維三路57巷37號9樓之4
          div.h-6.flex.mt-2
            img.h-full.p-1(src="{phoneIcon}" alt="phone")
            p.ml-2 +886 972322333
        div.mx-12.mt-8
          iframe.w-full.h-96(src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3682.95978328861!2d120.30820457549315!3d22.617976931305407!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x346e049c94bb90a7%3A0xfeb56573d9c9549c!2zODAy6auY6ZuE5biC6IuT6ZuF5Y2A5Zub57at5LiJ6LevNTflt7czN-iZnw!5e0!3m2!1szh-TW!2stw!4v1728062840137!5m2!1szh-TW!2stw" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade")
</template>

<style>
  .contact-container {
    height: calc(100vh - 96px);
  }

  p{
    font-family: "futura-pt", sans-serif;
    font-style: normal;
  }
</style>
