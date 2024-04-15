<section class="center w-full h-mn-100vh p-2rem ph-10vw">
  <header class="ta-center">
    <h1 class="fs-2.4rem">Svelte x TenoxUI App</h1>
    <p class="mb-2rem tc-#aaa fs-14px">
      Try tenoxui! It's fast, sometimes :D
    </p>
    <p class="tc-gray fs-12px">Edit <code>/src/App.svelte</code></p>
  </header>
</section>
<footer class="center w-full position-fixed b-0 p-1rem">
  <p class="fs-12px tc-#aaa">&copy; 2024 NOuSantx. Built with tenoxui/css</p>
</footer>

<script>
import { onMount } from 'svelte';
import tenoxui, { defineProps as makeProps, makeStyles } from "@tenoxui/react";

onMount(() => {
  // adding new props
  makeProps({
    // type example
    d: "display",
  });
  // define styles
  makeStyles({
    // styler example
    body: "bg-#0d0d0d tc-white family-[font-body] m-0",
    code: "bg-[code-back] ph-6px pv-2px br-0.125rem fs-inherit",
    // reusable class example
    ".center": "d-flex flex-parent-center",
    ".w-full": "w-100%",
  });
  // init tenoxui
  tenoxui();
});
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Gabarito:wght@400..900&display=swap");
:root {
  --font-body: "gabarito", sans-serif;
  --primary: #ccf654;
  --code-back: rgba(34, 34, 34, 0.3);
}
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
</style>