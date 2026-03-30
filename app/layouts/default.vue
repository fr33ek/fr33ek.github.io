<template>
  <div
    class="flex min-h-dvh min-h-[100dvh] flex-col bg-[#070708] bg-[radial-gradient(ellipse_120%_80%_at_50%_-20%,rgba(139,92,246,0.12),transparent)] text-zinc-200 antialiased selection:bg-violet-500/25"
  >
    <div class="min-h-0 flex-1">
      <slot />
    </div>
    <footer class="border-t border-zinc-800/50 py-10 text-center text-xs text-zinc-600">
      fr33ek · Санкт-Петербург
    </footer>
  </div>
</template>
