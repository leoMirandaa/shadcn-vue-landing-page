<script setup lang="ts">
import { type HTMLAttributes, computed } from "vue";
import {
  AccordionItem,
  type AccordionItemProps,
  useForwardProps,
} from "radix-vue";
import { cn } from "@/lib/utils";

const props = defineProps<
  AccordionItemProps & { class?: HTMLAttributes["class"] }
>();

const delegatedProps = computed(() => {
  const { class: _, ...delegated } = props;

  return delegated;
});

const forwardedProps = useForwardProps(delegatedProps);
</script>

<template>
  <AccordionItem
    v-bind="forwardedProps"
    :class="
      cn(
        'border-b bg-muted/50 dark:bg-card px-4 my-4 border rounded-lg',
        props.class
      )
    "
  >
    <slot />
  </AccordionItem>
</template>
