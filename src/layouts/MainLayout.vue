<template>
  <q-layout view="hHh lpR fFf">

    <q-header elevated class="bg-primary text-white" height-hint="98">
      <q-toolbar>
        <q-toolbar-title>
          <q-avatar>
            <label>&#128008;</label>
          </q-avatar>
          Котымания
        </q-toolbar-title>
      </q-toolbar>

      <q-tabs align="left">
        <q-route-tab to="/page1" label="О кошках" />
        <q-route-tab to="/page2" label="Игры" />
        <q-route-tab to="/page3" label="Форум" />
      </q-tabs>
    </q-header>

    <q-page-container>
      <div class="flex flex-center" style="max-width: 440px; margin: 60px;">
        <q-img class="q-mt-xl" src="https://loremflickr.com/640/360"></q-img>
        <div class="text-center q-mt-md">
          <p>Добро пожаловать на наш сайт о котиках! Здесь вы найдете всю необходимую информацию о ваших
            маленьких питомцах, которые становятся неотъемлемой частью нашей жизни. Мы стремимся предоставить вам
            полезные советы, интересные
            факты и многое другое о наших кошачьих друзьях.</p>
        </div>
        <q-btn style="background: goldenrod; color: white" label="Click me" />
      </div>
    </q-page-container>

    <q-footer elevated class="bg-grey-8 text-white">
      <q-toolbar>
        <q-toolbar-title>
          <q-avatar>
            <label>&#128062;</label>
          </q-avatar>
          <div>Мяу</div>
        </q-toolbar-title>
      </q-toolbar>
    </q-footer>

  </q-layout>
</template>

<script setup>
import { ref } from 'vue'
import EssentialLink from 'components/EssentialLink.vue'

defineOptions({
  name: 'MainLayout'
})

const linksList = [
  {
    title: 'Docs',
    caption: 'quasar.dev',
    icon: 'school',
    link: 'https://quasar.dev'
  },
  {
    title: 'Github',
    caption: 'github.com/quasarframework',
    icon: 'code',
    link: 'https://github.com/quasarframework'
  },
  {
    title: 'Discord Chat Channel',
    caption: 'chat.quasar.dev',
    icon: 'chat',
    link: 'https://chat.quasar.dev'
  },
  {
    title: 'Forum',
    caption: 'forum.quasar.dev',
    icon: 'record_voice_over',
    link: 'https://forum.quasar.dev'
  },
  {
    title: 'Twitter',
    caption: '@quasarframework',
    icon: 'rss_feed',
    link: 'https://twitter.quasar.dev'
  },
  {
    title: 'Facebook',
    caption: '@QuasarFramework',
    icon: 'public',
    link: 'https://facebook.quasar.dev'
  },
  {
    title: 'Quasar Awesome',
    caption: 'Community Quasar projects',
    icon: 'favorite',
    link: 'https://awesome.quasar.dev'
  }
]

const leftDrawerOpen = ref(false)

function toggleLeftDrawer () {
  leftDrawerOpen.value = !leftDrawerOpen.value
}
</script>
