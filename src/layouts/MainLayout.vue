<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <div class="b-header">
        <div class="b-header__bg"></div>
        <div class="b-header__title-container">
          <div class="b-header__title">SOUND</div>
          <div class="b-header__title-small">STORE</div>
        </div>
        <div class="b-header__right-block right-block">
          <div class="right-block__search"></div>
          <div class="right-block__card">Card</div>
          <div class="right-block__favorites">Favorites</div>
        </div>
      </div>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script lang="ts">
import { Vue, Component } from 'vue-property-decorator'

@Component({
  components: { }
})
export default class MainLayout extends Vue {
  leftDrawerOpen = false
}
</script>

