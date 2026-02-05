<template>
  <div class="flex flex-col w-full h-96 rounded-lg overflow-hidden relative">
    <!-- banner -->
     <div class="bg-primary font-bold">BANNER</div>

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
          Un asistente impulsado por IA para ayudarte con la documentación de Spartan.
        </p>
      </div>
    </div>

    <div class="p-3">
      <form
        class="flex items-center gap-2"
      >
        <UInput
          :disabled="true"
          placeholder="¿Hay algún componente para notificaciones?"
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