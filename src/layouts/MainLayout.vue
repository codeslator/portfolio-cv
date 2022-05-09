<template>
  <q-layout view="hHh LpR fFf">
    
    <!-- <q-drawer side="left" bordered>
      <q-toolbar />
      <q-separator />
      <q-list>
        <q-item clickable>
          <q-item-section>Single line item</q-item-section>
        </q-item>
      </q-list>
    </q-drawer> -->

    <layout-header />
    <q-page-container>
      <router-view />
    </q-page-container>
    <layout-footer />
  </q-layout>
</template>

<script lang="ts" setup>
import LayoutHeader from 'src/components/layout/LayoutHeader.vue';
import LayoutFooter from 'src/components/layout/LayoutFooter.vue';
</script>
