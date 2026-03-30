<script setup lang="ts">
useSeoMeta({
  title: 'Обо мне — fr33ek',
  description:
    'Team Lead / Lead Fullstack: НОНА ТЕХНОЛОГИИ, T-Systems, стек, сертификаты и продукты.',
  ogImage: '/images/profile.jpg'
})

const skillGroups = [
  {
    title: 'Управление и процессы',
    items: [
      'Team Lead',
      'Scrum Master (PSM I)',
      'найм и менторство',
      'ретроспективы',
      'бэклог со стейкхолдерами',
      'Jira, Confluence, Notion, Yandex Tracker',
      'интеграция трекеров с GitLab CI/CD'
    ]
  },
  {
    title: 'Технологии',
    items: [
      'PHP, Symfony, API Platform',
      'Vue.js, Nuxt, TypeScript',
      'REST, real-time',
      'Docker, Yandex Cloud',
      'MySQL, PostgreSQL',
      'PHPUnit, Behat, Robot Framework',
      'Python (скрипты, автотесты)'
    ]
  }
]

const experience = [
  {
    role: 'Co-Founder / Tech Lead',
    company: 'НОНА ТЕХНОЛОГИИ',
    period: 'март 2021 — по настоящее время',
    points: [
      'Команда 3–7 человек: Symfony, API Platform, Mercure; фронтенд на Vue, Nuxt, Quasar, TypeScript.',
      'Скрам-мастеринг, ретроспективы, трекеры и связка с CI/CD.',
      'Архитектура API и интеграций, техдолг, облако (Docker, Yandex Cloud).'
    ]
  },
  {
    role: 'Development Team Lead',
    company: 'T-Systems Russia',
    period: 'апрель 2012 — декабрь 2022',
    points: [
      'Кросс-функциональная команда 3–7: бэкенд, фронтенд, QA, DevOps; корпоративные веб-приложения, SAFe.',
      'Скрам, Jira, GitLab; автоматизация тестов (Robot Framework и др.).',
      'Стек: PHP, Vue.js, MySQL, Docker.'
    ]
  }
]

const products = [
  { name: 'wi.app', href: 'https://wi.app' },
  { name: 'wizg.app', href: 'https://wizg.app' },
  { name: 'resisto.tech', href: 'https://resisto.tech' },
  { name: 'wihooks.ru', href: 'https://wihooks.ru' },
  { name: '2pix.agency', href: 'https://2pix.agency' },
  { name: 'roundy.ru', href: 'https://roundy.ru' },
  { name: 'feedot.com', href: 'https://feedot.com' }
]

const certificates = [
  'Professional Scrum Master I (PSM I) — Scrum.org, 2019',
  'Zend Certified Engineer (ZCE) — Zend Technologies, 2016',
  'Эффективное взаимодействие в команде — Schouten Russia, 2015',
  'Проведение технического интервью — BusinessLink Training, 2015'
]
</script>

<template>
  <article class="space-y-12">
    <header class="flex flex-col gap-8 sm:flex-row sm:items-start sm:gap-10">
      <div class="mx-auto shrink-0 sm:mx-0">
        <img
          src="/images/profile.jpg"
          width="943"
          height="1280"
          alt="Фотография"
          class="h-56 w-auto max-w-[13rem] rounded-2xl border border-slate-700/80 object-cover object-top shadow-xl shadow-black/40 sm:h-72 sm:max-w-[15rem]"
          decoding="async"
          fetchpriority="high"
        />
      </div>
      <div class="min-w-0 flex-1 space-y-3 text-center sm:text-left">
        <p class="text-sm font-medium uppercase tracking-widest text-emerald-500/90">
          Профиль
        </p>
        <h1 class="text-3xl font-bold tracking-tight text-white sm:text-4xl">
          Обо мне
        </h1>
        <p class="text-slate-400">
          Team Lead / Tech Lead / Lead Fullstack — продукты и R&D, 10+ лет опыта ведения команд.
        </p>
      </div>
    </header>

    <section class="space-y-4 text-slate-300 leading-relaxed">
      <h2 class="text-lg font-semibold text-white">Кратко</h2>
      <p>
        Team Lead и Lead Fullstack с 10+ годами опыта управления кросс-функциональными командами
        (3–7 человек: бэкенд, фронтенд, QA, DevOps) в продуктовых и корпоративных проектах.
        Отвечал за результат, мотивацию и развитие людей, за найм и менторство (в НОНА и
        T-Systems). Тесно работал с продакт-менеджерами и стейкхолдерами: приоритизация бэклога,
        технические решения под бизнес, баланс скорости и качества.
      </p>
      <p>
        Выстраивал гибкие процессы при меняющихся приоритетах (Agile/Scrum, PSM I). Совмещал роль
        скрам-мастера: ретроспективы, настройка скрам-процессов, эксперименты с инструментами и
        интеграциями с CI/CD. Техническое видение: ревью архитектуры, управление техдолгом,
        инженерные практики; представлял команду и доносил решения до нетехнических коллег.
      </p>
      <p>
        Сооснователь продуктовой компании
        <strong class="font-medium text-slate-200">НОНА ТЕХНОЛОГИИ</strong>: вывод нескольких
        продуктов от идеи до продакшена. Основной стек:
        <strong class="font-medium text-slate-200"
          >PHP, Symfony, API Platform, Vue.js, Nuxt, TypeScript, Docker, Yandex Cloud</strong
        >; в командах были разные стеки. Для скриптов, техподдержки и автотестов использовал в том
        числе Python (Robot Framework в T-Systems; доработки с Cursor в НОНА). Сильный
        бэкенд-бэкграунд и опыт во фронтенде; ценю проактивность, эмпатию и поиск компромиссов.
      </p>
    </section>

    <section
      class="rounded-2xl border border-slate-800 bg-slate-900/40 p-6 sm:p-8 space-y-3"
    >
      <h2 class="text-lg font-semibold text-white">Проект QuizMaster</h2>
      <p class="text-slate-300 leading-relaxed">
        Отдельный продукт — Telegram Mini App для создания и проведения интерактивных квизов:
        конструктор, live и асинхронные режимы, статистика, монетизация Free/Premium. На фронтенде —
        Vue 3 (Composition API), TypeScript, Tailwind CSS, Telegram WebApp SDK, Vue Router и Pinia;
        на бэкенде — Python 3.12, FastAPI, PostgreSQL, Redis и WebSocket для live-игр.
      </p>
    </section>

    <section class="space-y-6">
      <h2 class="text-lg font-semibold text-white">Опыт</h2>
      <ul class="space-y-8">
        <li
          v-for="job in experience"
          :key="job.company"
          class="border-l-2 border-emerald-500/50 pl-5"
        >
          <h3 class="font-semibold text-white">{{ job.role }}</h3>
          <p class="text-sm text-emerald-400/90">{{ job.company }} · {{ job.period }}</p>
          <ul class="mt-3 list-disc space-y-2 pl-4 text-slate-400">
            <li v-for="(point, i) in job.points" :key="i">{{ point }}</li>
          </ul>
        </li>
      </ul>
    </section>

    <section class="space-y-4">
      <h2 class="text-lg font-semibold text-white">Навыки</h2>
      <div class="grid gap-6 sm:grid-cols-2">
        <div
          v-for="group in skillGroups"
          :key="group.title"
          class="rounded-xl border border-slate-800 bg-slate-900/30 p-5"
        >
          <h3 class="text-sm font-semibold uppercase tracking-wide text-slate-500">
            {{ group.title }}
          </h3>
          <ul class="mt-3 flex flex-wrap gap-2">
            <li
              v-for="item in group.items"
              :key="item"
              class="rounded-full bg-slate-800/80 px-3 py-1 text-xs text-slate-300"
            >
              {{ item }}
            </li>
          </ul>
        </div>
      </div>
    </section>

    <section class="space-y-3">
      <h2 class="text-lg font-semibold text-white">Образование</h2>
      <p class="text-slate-300">
        ЛГУ им. А.С. Пушкина, 2006–2011. Специалист, информатик-экономист (диплом с отличием,
        средний балл 4.9).
      </p>
    </section>

    <section class="space-y-3">
      <h2 class="text-lg font-semibold text-white">Сертификаты</h2>
      <ul class="list-disc space-y-2 pl-5 text-slate-400">
        <li v-for="c in certificates" :key="c">{{ c }}</li>
      </ul>
    </section>

    <section class="space-y-3">
      <h2 class="text-lg font-semibold text-white">Языки</h2>
      <p class="text-slate-300">
        Русский — родной. Английский — свободное владение (профессиональный). Немецкий — базовый.
      </p>
    </section>

    <section class="space-y-3">
      <h2 class="text-lg font-semibold text-white">Продукты и проекты</h2>
      <ul class="flex flex-wrap gap-2">
        <li v-for="p in products" :key="p.href">
          <a
            :href="p.href"
            class="inline-block rounded-lg border border-slate-700 bg-slate-900/50 px-3 py-1.5 text-sm text-emerald-400 transition hover:border-emerald-500/50 hover:text-emerald-300"
            target="_blank"
            rel="noopener noreferrer"
          >
            {{ p.name }}
          </a>
        </li>
      </ul>
    </section>

    <p class="text-sm text-slate-500">
      Условия: полная занятость; гибрид или удалённо, удобен офис в Санкт-Петербурге.
    </p>
  </article>
</template>
