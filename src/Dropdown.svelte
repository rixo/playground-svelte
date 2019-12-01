<script>
  import { onMount } from 'svelte'
  import jQuery from 'jquery'

  onMount(async () => {
    if (!window.jQuery) window.jQuery = jQuery
    await import('../semantic/dist/components/transition.js')
    await import('../semantic/dist/components/dropdown.js')
    jQuery('.ui.selection.dropdown').dropdown()
  })
</script>

<svelte:head>
  <link
    rel="stylesheet"
    type="text/css"
    href="/semantic/components/reset.css" />
  <link
    rel="stylesheet"
    type="text/css"
    href="/semantic/components/transition.css" />
  <link
    rel="stylesheet"
    type="text/css"
    href="/semantic/components/dropdown.css" />
</svelte:head>

<div class="ui selection dropdown">
  <input type="hidden" name="gender" />
  <i class="dropdown icon" />
  <div class="default text">Gender</div>
  <div class="menu">
    <div class="item" data-value="1">Male</div>
    <div class="item" data-value="0">Female</div>
  </div>
</div>
