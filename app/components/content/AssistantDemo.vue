<script setup lang="ts">
defineProps<{
  placeholder: string;
}>();
</script>

<template>
  <div class="flex flex-col w-full h-96 rounded-lg overflow-hidden">
    <!-- banner -->
     <div class="flex items-center gap-2 bg-inverted font-bold top-0 right-0 rotate-45 translate-y-full translate-x-1/4 absolute text-inverted px-2 py-1 shadow-lg rounded-xl">
      <UColorModeImage
        class="h-5"
        light="/landing/dark/evertec.svg"
        dark="/landing/light/evertec.svg"
        alt="Banner"
      />

      <slot name="banner" />

      <span>💸</span>
     </div>

    <div class="flex-1 overflow-y-auto">
      <div
        class="h-full flex flex-col items-center justify-center p-4 text-center"
      >
        <div class="size-10 rounded-full bg-muted/10 flex items-center justify-center mb-3">
          <UIcon
            name="i-lucide-sparkles"
            class="size-5 text-muted"
          />
        </div>
        <p class="text-sm text-muted">
          <slot />
        </p>
      </div>
    </div>

    <div class="p-3">
      <form
        class="flex items-center gap-2"
      >
        <UInput
          :disabled="true"
          :placeholder
          size="sm"
          class="flex-1"
          :ui="{
            base: 'bg-elevated',
          }"
        />
        <div class="flex items-center gap-1">
          <UButton
            type="submit"
            icon="i-lucide-arrow-up"
            color="primary"
            size="xs"
            :disabled="true"
          />
        </div>
      </form>
    </div>
  </div>
</template>