<script>
  const { label = 'A Very Important Checkbox', id = 'checkbox', ...props } = $props();
</script>

<div class="rounded-border bg-slate-200 px-4 outline focus-within:bg-sky-200">
  <input class="peer accent-amber-50" {id} {...props} type="checkbox" />
  <label class="peer-checked:line-through" for={id}>{label}</label>
</div>
