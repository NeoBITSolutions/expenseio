<script lang="ts">
  import { cn } from "$lib/utils";
  import type { WithElementRef } from "bits-ui";
  import type { HTMLThAttributes } from "svelte/elements";

  let {
    ref = $bindable(null),
    class: className,
    children,
    ...restProps
  }: WithElementRef<HTMLThAttributes> = $props();
</script>

<th
  bind:this={ref}
  class={cn(
    "h-12 px-4 text-left align-middle font-medium text-muted-foreground [&:has([role=checkbox])]:pr-0",
    className
  )}
  {...restProps}>
  {@render children?.()}
</th>
