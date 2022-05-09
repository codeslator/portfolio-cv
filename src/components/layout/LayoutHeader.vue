<template>
  <q-header reveal elevated class="text-black" :class="$q.dark.isActive ? 'bg-primary' : 'bg-secondary'">
    <q-toolbar>
      <q-btn dense flat round icon="menu" class="lt-md" @click="toggleLeftDrawer" />
      <q-toolbar-title class="code_source">
        <q-avatar>
          <img src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-white.svg">
        </q-avatar>
        {{ `
        <CODESLATOR />`}}
      </q-toolbar-title>
      <div class="gt-sm">
        <q-btn flat label="<About me>" class="code_source text-weight-bold" />
        <q-btn flat label="<Services>" class="code_source text-weight-bold" />
        <q-btn flat label="<Skills>" class="code_source text-weight-bold" />
        <q-btn flat label="<Projects>" class="code_source text-weight-bold" />
        <q-btn flat label="<Courses>" class="code_source text-weight-bold" />
        <q-btn flat label="<Contact>" class="code_source text-weight-bold" />
      </div>
      <q-btn round outline dense color="black" :icon="$q.dark.isActive ? 'light_mode' : 'dark_mode'"
        @click="$q.dark.toggle" />
    </q-toolbar>
  </q-header>
</template>

<script lang="ts" setup>
import { ref } from 'vue';
import { useQuasar } from 'quasar'
const $q = useQuasar();

const leftDrawerOpen = ref(false);
const toggleLeftDrawer = () => {
  leftDrawerOpen.value = !leftDrawerOpen.value
}
</script>