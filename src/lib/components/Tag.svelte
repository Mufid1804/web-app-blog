<script lang="ts">
    export let label: string;
    export let href = "#";
  </script>
  
  <a href={href} class="chip variant-filled bg-secondary-600 hover:bg-secondary-900">{label}</a>
  