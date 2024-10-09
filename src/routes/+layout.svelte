<script lang="ts">
  import { page } from '$app/stores';
  import "../app.css";
  import logo from "../lib/images/eco_trade_logo.png"
  import textlogo from "../lib/images/logo_text.png"
  import menu from "../lib/images/menu.png"
  import { isDrawerOpen } from "../lib/ts/store";
  import { initializeStores, getDrawerStore, Drawer } from "@skeletonlabs/skeleton";

  var currentPage = ""
  $: currentPage = $page.url.pathname
  $: innerWidth = 0

  initializeStores();
  $: drawerStore = getDrawerStore()

  function clickDrawer() {
    $isDrawerOpen = !$isDrawerOpen
    if ($isDrawerOpen) {
        const menuDrawerSettings = {
            position: "right",
            bgDrawer: "bg-[#FFFFFF]",
            width: "w-96",
            height: "h-screen",
        }
        drawerStore.open(menuDrawerSettings)
    }
    else {
        drawerStore.close()
    }
  }
</script>

<svelte:window bind:innerWidth/>
<template lang="pug">
  header.w-screen.z-50
    div.flex.flex-row-reverse
      Drawer.mt-24
        div.grid.grid-cols-1
          hr
          a.text-3xl.my-2.ml-4(href="/profile" on:click!="{() => clickDrawer()}") Profile
          hr
          a.text-3xl.my-2.ml-4(href="/products" on:click!="{() => clickDrawer()}") Products
          hr
          a.text-3xl.my-2.ml-4(href="contact" on:click!="{() => clickDrawer()}") Contact
    div.w-full.mt-4.flex
      div.flex.h-20.p-1(class="w-full")
        a(href="/profile")
          img.h-full(src="{logo}" alt="logo" class="ml-8")
        a(href="/profile")
          img.h-full(src="{textlogo}" alt="textlogo")
      +if("innerWidth > 1024")
        div.grid.justify-items-end(class="w-3/4")
          div.flex.flex-row-reverse.text-lg.items-center.mr-24
            button.ml-16.btn(class="invisible lg:visible")
              a(href="/contact" class="{currentPage == '/contact' ? 'selected' : 'unselected'}") Contact
            button.ml-16.btn(class="invisible lg:visible")
              a(href="/products" class="{currentPage == '/products' || currentPage == '/filter' || currentPage == '/chiller' ? 'selected' : 'unselected'}") Products
            button.ml-16.btn(class="invisible lg:visible")
              a(href="/profile" class="{currentPage == '/profile' ? 'selected' : 'unselected'}") Profile
        +else
          button.h-12.mr-8.mt-4.visible(on:click!="{() => clickDrawer()}")
            img.h-12(src="{menu}" alt="menu")
  div.h-24
  div.content-container
    slot
</template>

<style>
  header {
    position: fixed;
    height: 96px;
    top: 0px;
    background-color: white;
  }

  a {
    font-family: "futura-pt", sans-serif;
    font-weight: 500;
    font-style: normal;
  }

  .content-container {
    height: calc(100vh - 96px);
  }

  .btn{
    font-family: "futura-pt", sans-serif;
    font-weight: 500;
    font-style: normal;
    background: transparent;
    border: none;
    display: block;
    outline: none;
    position: relative;
    transition: 0.3s;
    padding: 10px;
    color: #393D3F;
  }
  .unselected::before {
      content: '';
      border-bottom: 2px solid #BC6172;
      position: absolute;
      bottom: 0;
      left: 0;
      right: 0;
      margin: 0 auto;
      width: 0;
      transition: 0.3s;
  }
  .unselected:hover::before {
      width: 70%;
      padding: 0;
  }

  .unselected:hover {
      color: #BC6172;
  }

  .selected {
    color: #BC6172;
  }

  .unselected {
    color: #393D3F;
  }
</style>
