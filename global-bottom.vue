<template>
  <footer class="absolute bottom-0 left-0 right-0 w-full z-9">
    <div
      class="flex w-full p-2"
      :class="{
        'justify-start': $slidev.configs.globalBottomPosition === 'left',
        'justify-end': !$slidev.configs.globalBottomPosition,
      }"
    >
      <div
        class="flex flex-col gap-2 bg-light-background dark:bg-dark-background bg-opacity-60 p-2 rounded-md logo"
      >
        <img src="/bcc-logo.png" alt="bcc" width="12%" />
      </div>
      <div class="flex items-center mr-4">
        <SlideCurrentNo /> / <SlidesTotal />
      </div>
    </div>
    <!-- <div class="border-bar"></div> -->
  </footer>
</template>

<style>
.border-bar {
  @apply h-0.5 w-full mb-1 bg-accent;
  box-shadow: 0 0 3px 0.5px var(--accent);
}
</style>
