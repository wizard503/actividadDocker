<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="drawer = !drawer"
        />

        <q-toolbar-title>
          <strong> Diseño de Sistemas I </strong>
        </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-footer bordered>
      <q-toolbar>
        <q-toolbar-title align="center">Grupo 1</q-toolbar-title>
      </q-toolbar>
    </q-footer>

    <q-drawer v-model="drawer" show-if-above :width="200" :breakpoint="400">
      <q-scroll-area
        style="
          height: calc(100% - 150px);
          margin-top: 150px;
          border-right: 1px solid #ddd;
        "
      >
        <q-list>
          <q-separator />
          <q-item clickable v-ripple to="/proyecto">
            <q-item-section avatar>
              <q-icon name="code" />
            </q-item-section>
            <q-item-section> Mi Proyecto </q-item-section>
          </q-item>
          <q-separator />
          <q-item active clickable v-ripple to="/card">
            <q-item-section avatar>
              <q-icon name="school" />
            </q-item-section>

            <q-item-section> Mi Conocimiento </q-item-section>
          </q-item>
          <br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br />
          <q-item active clickable v-ripple to="/">
            <q-item-section avatar>
              <q-icon name="home" />
            </q-item-section>

            <q-item-section> Home </q-item-section>
          </q-item>
        </q-list>
      </q-scroll-area>

      <q-img
        class="absolute-top"
        src="https://png.pngtree.com/thumb_back/fw800/background/20190221/ourmid/pngtree-3d-stereoscopic-property-technology-image_26567.jpg"
        style="height: 150px"
      >
        <div class="absolute-bottom bg-transparent">
          <q-avatar size="56px" class="q-mb-sm">
            <img src="https://cdn.quasar.dev/img/boy-avatar.png" />
          </q-avatar>
          <div class="text-weight-bold">
            <strong>José Magdiel<br />Durán Guerra</strong>
          </div>
          <div>DG17001</div>
        </div>
      </q-img>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    return {
      drawer: ref(false),
    };
  },
};
</script>
