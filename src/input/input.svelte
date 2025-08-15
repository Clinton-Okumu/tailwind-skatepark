<script>
  const { id = 'input', label, description, error, ...props } = $props();
  const descriptionId = description ? `${id}-description` : undefined;
  const errorId = error ? `${id}-error` : undefined;
</script>

<div class="space-y-2">
  <label class="block font-medium text-slate-900" for={id}>{label}</label>
  <input
    class="block w-full rounded-md bg-white px-1 py-1 outline outline-slate-200 focus:outline-blue-600"
    {id}
    aria-describedby={descriptionId}
    aria-invalid={!!error}
    aria-errormessage={errorId}
    {...props}
  />
  {#if description}
    <p id={descriptionId}>{description}</p>
  {/if}
  {#if error}
    <p id={errorId}>{error}</p>
  {/if}
</div>
