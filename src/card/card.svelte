<script>
  const { title = 'Card Title', description = '' } = $props();
</script>

<div class="rounded-sm border-2 border-slate-200 bg-slate-200 p-4">
  <h2 class="text-xl font-bold">{title}</h2>
  <p class="mt-1">{description}</p>
</div>
