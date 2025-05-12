<script lang="ts">
  import { cn } from "$lib/utils";
  import type { WithoutChild } from "bits-ui";
  import * as FormPrimitive from "formsnap";

  let {
    ref = $bindable(null),
    class: className,
    ...restProps
  }: WithoutChild<FormPrimitive.LegendProps> = $props();
</script>

<FormPrimitive.Legend
  bind:ref
  class={cn("data-[fs-error]:text-danger text-sm font-medium leading-none", className)}
  {...restProps} />
