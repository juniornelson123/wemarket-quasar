<template>
  <q-layout view="lHh Lpr lFf bg-grey-3">
    <q-toolbar class="bg-orange text-white">
      <q-btn
        flat
        dense
        round
        @click="leftDrawerOpen = !leftDrawerOpen"
        icon="menu"
        aria-label="Menu"
      />

      <q-toolbar-title class="text-center titleHeader">
        WeMarket
      </q-toolbar-title>
      <q-btn flat round dense icon="search" />
    </q-toolbar>
    <q-footer reveal elevated class="bg-white footerApp">
      <q-toolbar>
        <div class="text-orange itemFooter left">
          <q-icon class="iconItemFooter" name="star" />favoritos
        </div>
        <q-btn fab icon="search" class="floatButton" color="orange" />
        <div class="text-orange itemFooter right">
          <q-icon class="iconItemFooter" name="list" />minha lista
        </div>
      </q-toolbar>
    </q-footer>
    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
      content-class="bg-grey-2"
    >
      <q-list>
        <q-item-label header>Essential Links</q-item-label>
        <q-item clickable tag="a" target="_blank" href="https://quasar.dev">
          <q-item-section avatar>
            <q-icon name="school" />
          </q-item-section>
          <q-item-section>
            <q-item-label>Docs</q-item-label>
            <q-item-label caption>quasar.dev</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable tag="a" target="_blank" href="https://github.quasar.dev">
          <q-item-section avatar>
            <q-icon name="code" />
          </q-item-section>
          <q-item-section>
            <q-item-label>Github</q-item-label>
            <q-item-label caption>github.com/quasarframework</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable tag="a" target="_blank" href="https://chat.quasar.dev">
          <q-item-section avatar>
            <q-icon name="chat" />
          </q-item-section>
          <q-item-section>
            <q-item-label>Discord Chat Channel</q-item-label>
            <q-item-label caption>chat.quasar.dev</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable tag="a" target="_blank" href="https://forum.quasar.dev">
          <q-item-section avatar>
            <q-icon name="record_voice_over" />
          </q-item-section>
          <q-item-section>
            <q-item-label>Forum</q-item-label>
            <q-item-label caption>forum.quasar.dev</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable tag="a" target="_blank" href="https://twitter.quasar.dev">
          <q-item-section avatar>
            <q-icon name="rss_feed" />
          </q-item-section>
          <q-item-section>
            <q-item-label>Twitter</q-item-label>
            <q-item-label caption>@quasarframework</q-item-label>
          </q-item-section>
        </q-item>
        <q-item clickable tag="a" target="_blank" href="https://facebook.quasar.dev">
          <q-item-section avatar>
            <q-icon name="public" />
          </q-item-section>
          <q-item-section>
            <q-item-label>Facebook</q-item-label>
            <q-item-label caption>@QuasarFramework</q-item-label>
          </q-item-section>
        </q-item>
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>


  </q-layout>
</template>

<style lang="scss">


  * {
    font-family: 'Montserrat Alternates', sans-serif;
  }

  .floatButton {
    position: absolute;
    right: 42%;
    top: -45%;

    &.q-icon {
      font-size: 100px;
    }
  }

  .titleHeader {
    font-weight: 600;
    font-size: 18px;
  }

  .footerApp{
    display: flex;
  }

  .iconItemFooter{
    margin-right: 5px;
  }

  .itemFooter{
    display: flex;
    width: 100%;
    align-items: center;

    &.left {
      margin-left: 20px;
    }

    &.right {
      margin-left: 53px;
    }
  }
</style>

<script>
export default {
  name: 'MyLayout',

  data () {
    return {
      leftDrawerOpen: false
    }
  }
}
</script>
