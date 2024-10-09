<script lang="ts">
  import { browser } from '$app/environment';
  import { goto } from '$app/navigation';

  $: if(browser) { goto("/profile") }
</script>

<template lang="pug">
</template>
