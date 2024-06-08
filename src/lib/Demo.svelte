<script>
  export let url;
  export let title;
</script>

<iframe
  {title}
  src="{import.meta.env.VITE_DEMO_URL}{url}"
  width="700"
  height="540"
  frameborder="0"
></iframe>

<style>
  iframe {
    border-radius: 15px;
    border: 2px solid rgb(255 255 255 / 0.3);
  }
</style>
