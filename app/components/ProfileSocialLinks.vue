<script setup lang="ts">
type ProfileSocialLink = {
  href: string
  label: string
  icon: 'telegram' | 'vk'
}

defineProps<{
  links: readonly ProfileSocialLink[]
  align?: 'center' | 'end'
}>()
</script>

<template>
  <div
    class="mt-3 flex gap-4"
    :class="align === 'end' ? 'justify-end' : 'justify-center'"
  >
    <a
      v-for="link in links"
      :key="link.href"
      :href="link.href"
      target="_blank"
      rel="noopener noreferrer"
      :aria-label="link.label"
      class="text-zinc-500 transition-colors duration-200 focus-visible:rounded-sm focus-visible:text-zinc-200 focus-visible:outline focus-visible:outline-1 focus-visible:outline-offset-2 focus-visible:outline-violet-500/40"
      :class="
        link.icon === 'telegram'
          ? 'hover:text-sky-400/85'
          : 'hover:text-[#5B9FFF]/90'
      "
    >
      <svg
        v-if="link.icon === 'telegram'"
        class="h-[1.125rem] w-[1.125rem]"
        viewBox="0 0 24 24"
        xmlns="http://www.w3.org/2000/svg"
        aria-hidden="true"
      >
        <path
          fill="currentColor"
          d="M11.944 0A12 12 0 0 0 0 12a12 12 0 0 0 12 12 12 12 0 0 0 12-12A12 12 0 0 0 12 0a12 12 0 0 0-.056 0zm4.962 7.224c.1-.002.321.023.465.14a.506.506 0 0 1 .171.325c.016.093.036.306.02.472-.18 1.898-.962 6.502-1.36 8.627-.168.9-.499 1.201-.82 1.23-.696.065-1.225-.46-1.9-.902-1.056-.693-1.653-1.124-2.678-1.8-1.185-.78-.417-1.21.258-1.91.177-.184 3.247-2.977 3.307-3.23.007-.032.014-.15-.056-.212s-.174-.041-.249-.024c-.106.024-1.793 1.14-5.061 3.345-.48.33-.913.49-1.302.48-.428-.008-1.252-.241-1.865-.44-.752-.245-1.349-.374-1.297-.789.027-.216.325-.437.893-.663 3.498-1.524 5.83-2.529 6.998-3.014 3.332-1.386 4.025-1.627 4.476-1.635z"
        />
      </svg>
      <svg
        v-else
        class="h-[1.125rem] w-[1.125rem]"
        viewBox="0 0 24 24"
        xmlns="http://www.w3.org/2000/svg"
        aria-hidden="true"
      >
        <path
          fill="currentColor"
          d="M15.684 0H8.316C1.592 0 0 1.592 0 8.316v7.368C0 22.408 1.592 24 8.316 24h7.368C22.408 24 24 22.408 24 15.684V8.316C24 1.592 22.391 0 15.684 0zm3.692 17.316h-1.744c-.66 0-.862-.525-2.05-1.727-1.033-1-1.49-1.135-1.744-1.135-.356 0-.458.102-.458.593v1.575c0 .424-.135.678-1.253.678-1.846 0-3.896-1.118-5.335-3.179C4.834 10.713 4.32 8.316 4.32 7.865c0-.254.102-.491.593-.491h1.744c.44 0 .61.203.78.677.863 2.491 2.303 4.675 2.896 4.675.22 0 .322-.102.322-.66V9.721c-.068-1.186-.695-1.287-.695-1.71 0-.203.17-.407.44-.407h2.744c.373 0 .508.203.508.643v4.675c0 .372.17.508.271.508.22 0 .407-.135.813-.542 1.254-1.389 2.15-3.537 2.15-3.537.119-.254.322-.491.763-.491h1.744c.525 0 .644.271.525.643-.22 1.017-2.354 4.031-2.354 4.031-.186.305-.254.44 0 .78.186.254.796.847 1.203 1.355.744.847 1.32 1.558 1.473 2.05.17.491-.085.744-.576.744z"
        />
      </svg>
    </a>
  </div>
</template>
