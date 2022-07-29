<template>
  <main id="main" class="main">
    <!-- App Before -->
    <slot name="app-before" />
    <div id="app-before"></div>

    <!-- App Content -->
    <div class="flex flex-col">
      <slot name="header">
        <PageNavbar />
      </slot>
      <div class="container w-full h-full flex flex-col sm:pb-16 <sm:pb-16 md:pb-0">
        <slot />
      </div>
    </div>

    <!-- App After -->
    <slot name="app-after" />
    <div id="app-after"></div>
  </main>
</template>
