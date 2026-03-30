<script setup lang="ts">
useHead({
  htmlAttrs: { class: 'scroll-smooth' }
})

useSeoMeta({
  title: 'fr33ek',
  description:
    'Разработчик и техлид из Санкт-Петербурга: продукты, команды и продуктовая разработка.',
  ogImage: '/images/profile.jpg'
})

const facts = [
  { key: 'Город', value: 'Санкт-Петербург' },
  { key: 'Роли', value: 'Co-founder, tech lead, fullstack' },
  { key: 'Сейчас', value: 'НОНА ТЕХНОЛОГИИ — продукты и команда' },
  { key: 'Раньше', value: 'T-Systems — корпоративные веб-приложения, ~10 лет' }
]

const stack = [
  'PHP',
  'TypeScript',
  'Python',
  'Symfony',
  'API Platform',
  'FastAPI',
  'Mercure',
  'Vue',
  'Nuxt',
  'Quasar',
  'Tailwind CSS',
  'Pinia',
  'PostgreSQL',
  'MySQL',
  'Redis',
  'Docker',
  'GitLab',
  'Yandex Cloud',
  'Cursor'
]

const processThings = [
  'Scrum / Agile',
  'CI/CD',
  'Code review',
  'TDD'
]

const projects = [
  { name: 'wi.app', href: 'https://wi.app' },
  { name: 'wizg.app', href: 'https://wizg.app' },
  { name: 'resisto.tech', href: 'https://resisto.tech' },
  { name: 'wihooks.ru', href: 'https://wihooks.ru' },
  { name: '2pix.agency', href: 'https://2pix.agency' }
]

const learning = [
  'PSM I — Scrum.org, 2019',
  'Zend Certified Engineer — 2016',
  'Schouten — командное взаимодействие, 2015',
  'BusinessLink — техсобеседования, 2015'
]

const profileSocial = [
  {
    href: 'https://t.me/fr33ek',
    label: 'Telegram',
    icon: 'telegram' as const
  },
  {
    href: 'https://vk.com/freeek',
    label: 'ВКонтакте',
    icon: 'vk' as const
  }
]
</script>

<template>
  <main class="mx-auto max-w-6xl px-4 pb-16 pt-10 sm:px-6 sm:pt-14 lg:pb-24">
    <div class="flex flex-col gap-14 lg:flex-row lg:gap-12 xl:gap-16">
      <!-- Контент слева на десктопе; на мобилке — после фото (order) -->
      <div class="min-w-0 flex-1 space-y-4 order-2 lg:order-1">
        <div class="mb-2 text-center lg:hidden">
          <p class="font-mono text-[10px] font-medium uppercase tracking-[0.2em] text-violet-400/90">
            profile.json
          </p>
          <h1 class="mt-2 text-3xl font-semibold tracking-tight text-white">fr33ek</h1>
          <ProfileSocialLinks :links="profileSocial" />
        </div>

        <div class="grid auto-rows-min grid-cols-1 gap-4 md:grid-cols-2">
          <!-- Intro -->
          <section
            class="group relative overflow-hidden rounded-3xl border border-zinc-800/80 bg-zinc-900/35 p-6 backdrop-blur-sm transition hover:border-zinc-700/80 md:col-span-2 md:p-8"
          >
            <div
              class="pointer-events-none absolute -right-20 -top-20 h-40 w-40 rounded-full bg-violet-600/10 blur-3xl transition group-hover:bg-violet-500/15"
            />
            <p class="font-mono text-[10px] font-medium uppercase tracking-[0.2em] text-zinc-500">
              01 — о себе
            </p>
            <p class="mt-4 max-w-3xl text-lg font-medium leading-relaxed text-zinc-100 md:text-xl">
              Привет! Я разработчик и техлид: люблю вести продукт от идеи до продакшена, собирать
              вокруг себя сильных людей и наводить порядок в архитектуре и процессах — без лишней
              суеты.
            </p>
            <p class="mt-4 max-w-3xl leading-relaxed text-zinc-400">
              Сооснователь
              <span class="text-zinc-300">НОНА ТЕХНОЛОГИИ</span>
              : вместе с командой выводим продукты от идеи до продакшена.
            </p>
          </section>

          <!-- Сейчас в работе -->
          <section
            class="rounded-3xl border border-zinc-800/80 bg-zinc-900/35 p-6 backdrop-blur-sm transition hover:border-sky-500/20"
          >
            <p class="font-mono text-[10px] font-medium uppercase tracking-[0.2em] text-zinc-500">
              02 — сейчас
            </p>
            <h2 class="mt-3 text-lg font-semibold text-white">Резисто</h2>
            <p class="mt-3 text-sm leading-relaxed text-zinc-400">
              <a
                href="https://resisto.tech"
                target="_blank"
                rel="noopener noreferrer"
                class="text-sky-400/95 underline decoration-sky-500/40 underline-offset-2 transition hover:text-sky-300"
              >
                Резисто
              </a>
              — наш новый продукт! Это платформа роста для автосалонов и автосервисов — клиенты,
              онлайн-запись, аналитика, лояльность и автоматизация коммуникаций (в т.ч. пуши вместо
              SMS). Развиваем продукт в команде и выкатываем в прод.
            </p>
          </section>

          <!-- Факты как «данные» -->
          <section
            class="rounded-3xl border border-zinc-800/80 bg-zinc-900/35 p-6 backdrop-blur-sm transition hover:border-violet-500/20"
          >
            <p class="font-mono text-[10px] font-medium uppercase tracking-[0.2em] text-zinc-500">
              03 — данные
            </p>
            <dl class="mt-4 space-y-4">
              <div v-for="row in facts" :key="row.key">
                <dt class="font-mono text-[11px] uppercase tracking-wider text-violet-400/80">
                  {{ row.key }}
                </dt>
                <dd class="mt-1 text-sm leading-snug text-zinc-300">{{ row.value }}</dd>
              </div>
            </dl>
          </section>

          <!-- Процессы -->
          <section
            class="rounded-3xl border border-zinc-800/80 bg-zinc-900/35 p-6 backdrop-blur-sm md:col-span-2"
          >
            <p class="font-mono text-[10px] font-medium uppercase tracking-[0.2em] text-zinc-500">
              04 — как работаю
            </p>
            <p class="mt-3 text-sm text-zinc-400">
              Коротко: прозрачная коммуникация, итерации, внимание к качеству и к людям.
            </p>
            <ul class="mt-4 flex flex-wrap gap-2">
              <li
                v-for="item in processThings"
                :key="item"
                class="rounded-full border border-zinc-700/60 bg-zinc-950/40 px-3 py-1.5 font-mono text-[11px] text-zinc-400"
              >
                {{ item }}
              </li>
            </ul>
          </section>

          <!-- Стек -->
          <section
            class="rounded-3xl border border-zinc-800/80 bg-zinc-900/35 p-6 backdrop-blur-sm md:col-span-2"
          >
            <p class="font-mono text-[10px] font-medium uppercase tracking-[0.2em] text-zinc-500">
              05 — стек
            </p>
            <ul class="mt-4 flex flex-wrap gap-2">
              <li
                v-for="tag in stack"
                :key="tag"
                class="rounded-lg border border-zinc-700/50 bg-zinc-950/50 px-2.5 py-1 text-xs font-medium text-zinc-300"
              >
                {{ tag }}
              </li>
            </ul>
          </section>

          <!-- Проекты -->
          <section
            class="rounded-3xl border border-zinc-800/80 bg-zinc-900/35 p-6 backdrop-blur-sm md:col-span-2"
          >
            <p class="font-mono text-[10px] font-medium uppercase tracking-[0.2em] text-zinc-500">
              06 — проекты и ссылки
            </p>
            <ul class="mt-4 flex flex-wrap gap-2">
              <li v-for="p in projects" :key="p.href">
                <a
                  :href="p.href"
                  target="_blank"
                  rel="noopener noreferrer"
                  class="inline-flex items-center gap-1.5 rounded-xl border border-zinc-700/60 bg-zinc-950/40 px-3 py-2 text-sm text-sky-400/95 transition hover:border-sky-500/40 hover:text-sky-300"
                >
                  {{ p.name }}
                  <span class="text-zinc-600" aria-hidden="true">↗</span>
                </a>
              </li>
            </ul>
          </section>

          <!-- Образование -->
          <section class="rounded-3xl border border-zinc-800/80 bg-zinc-900/35 p-6 backdrop-blur-sm">
            <p class="font-mono text-[10px] font-medium uppercase tracking-[0.2em] text-zinc-500">
              07 — образование
            </p>
            <p class="mt-4 text-sm leading-relaxed text-zinc-400">
              ЛГУ им. А.С. Пушкина, 2006–2011. Информатик-экономист, красный диплом, средний балл
              4.9.
            </p>
          </section>

          <!-- Языки + обучение -->
          <section class="rounded-3xl border border-zinc-800/80 bg-zinc-900/35 p-6 backdrop-blur-sm">
            <p class="font-mono text-[10px] font-medium uppercase tracking-[0.2em] text-zinc-500">
              08 — языки
            </p>
            <p class="mt-4 text-sm leading-relaxed text-zinc-400">
              Русский — родной. Английский — рабочий, свободно. Немецкий — базово, «на жизнь».
            </p>
            <p class="mt-6 font-mono text-[10px] font-medium uppercase tracking-[0.2em] text-zinc-500">
              курсы и сертификаты
            </p>
            <ul class="mt-3 space-y-2 text-xs leading-relaxed text-zinc-500">
              <li v-for="line in learning" :key="line">{{ line }}</li>
            </ul>
          </section>

          <!-- Контакты -->
          <section
            id="contact"
            class="relative overflow-hidden rounded-3xl border border-sky-500/25 bg-gradient-to-br from-sky-950/40 via-zinc-900/40 to-violet-950/30 p-6 backdrop-blur-sm md:col-span-2 md:p-8"
          >
            <div
              class="pointer-events-none absolute -bottom-24 -right-24 h-48 w-48 rounded-full bg-sky-500/10 blur-3xl"
            />
            <p class="font-mono text-[10px] font-medium uppercase tracking-[0.2em] text-sky-400/90">
              09 — контакты
            </p>
            <h2 class="mt-3 text-xl font-semibold text-white">Написать</h2>
            <p class="mt-2 max-w-xl text-sm leading-relaxed text-zinc-400">
              Удобнее всего в
              <a
                href="https://t.me/fr33ek"
                target="_blank"
                rel="noopener noreferrer"
                aria-label="Написать в Telegram, @fr33ek"
                class="font-medium text-sky-400/95 underline decoration-sky-500/40 underline-offset-2 transition hover:text-sky-300 hover:decoration-sky-400/50"
              >
                <svg
                  class="mr-1 inline-block h-[1em] w-[1em] align-[-0.15em] text-current"
                  viewBox="0 0 24 24"
                  xmlns="http://www.w3.org/2000/svg"
                  aria-hidden="true"
                >
                  <path
                    fill="currentColor"
                    d="M11.944 0A12 12 0 0 0 0 12a12 12 0 0 0 12 12 12 12 0 0 0 12-12A12 12 0 0 0 12 0a12 12 0 0 0-.056 0zm4.962 7.224c.1-.002.321.023.465.14a.506.506 0 0 1 .171.325c.016.093.036.306.02.472-.18 1.898-.962 6.502-1.36 8.627-.168.9-.499 1.201-.82 1.23-.696.065-1.225-.46-1.9-.902-1.056-.693-1.653-1.124-2.678-1.8-1.185-.78-.417-1.21.258-1.91.177-.184 3.247-2.977 3.307-3.23.007-.032.014-.15-.056-.212s-.174-.041-.249-.024c-.106.024-1.793 1.14-5.061 3.345-.48.33-.913.49-1.302.48-.428-.008-1.252-.241-1.865-.44-.752-.245-1.349-.374-1.297-.789.027-.216.325-.437.893-.663 3.498-1.524 5.83-2.529 6.998-3.014 3.332-1.386 4.025-1.627 4.476-1.635z"
                  />
                </svg>
                Telegram
              </a>
              — отвечу, когда буду онлайн.
            </p>
          </section>
        </div>
      </div>

      <!-- Фото справа на десктопе; на мобилке — сверху -->
      <aside
        class="order-1 flex shrink-0 flex-col items-center lg:order-2 lg:sticky lg:top-10 lg:w-[min(100%,280px)] lg:items-end xl:w-[300px]"
      >
        <div
          class="relative w-full max-w-[240px] overflow-hidden rounded-[1.75rem] border border-zinc-800/80 bg-zinc-900/40 shadow-2xl shadow-violet-950/20 ring-1 ring-white/5 sm:max-w-[260px] lg:max-w-none"
        >
          <div
            class="pointer-events-none absolute inset-0 bg-gradient-to-t from-[#070708]/40 via-transparent to-transparent"
          />
          <img
            src="/images/profile.jpg"
            width="943"
            height="1280"
            alt="fr33ek"
            class="aspect-[3/4] w-full object-cover object-top"
            decoding="async"
            fetchpriority="high"
          />
        </div>
        <div class="mt-8 hidden text-right lg:block lg:w-full">
          <p class="font-mono text-[10px] font-medium uppercase tracking-[0.2em] text-violet-400/90">
            profile.json
          </p>
          <p class="mt-2 text-2xl font-semibold tracking-tight text-white">fr33ek</p>
          <ProfileSocialLinks :links="profileSocial" align="end" />
        </div>
      </aside>
    </div>
  </main>
</template>
