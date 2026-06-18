<template>
  <q-layout view="lHr lpR fFf">

    <q-header bordered class="bg-pink-1 text-pink-10">
      <q-toolbar>
        <q-btn dense flat round icon="menu" @click="left = !left" color="pink-7" />

        <q-toolbar-title class="text-weight-bold text-pink-8">
          <span class="gt-sm">{{ $route.name }}</span>
          <q-icon
            class="header-icon q-pa-md lt-md"
            name="fas fa-dove"
            size="sm"
            color="pink-6"
          />
        </q-toolbar-title>

      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="left"
      side="left"
      :width="283"
      bordered
      class="bg-pink-1"
    >
      <q-icon
        class="q-pa-md"
        name="fas fa-dove"
        size="lg"
        color="pink-6"
      />

      <q-list>
        <q-item
          to="/"
          v-ripple
          clickable
          exact
          active-class="text-pink-8"
        >
          <q-item-section avatar>
            <q-icon name="home" size="md" color="pink-6" />
          </q-item-section>

          <q-item-section class="text-h6 text-weight-bold text-pink-9">Home</q-item-section>
        </q-item>
        <q-item
          to="/about"
          v-ripple
          clickable
          exact
          active-class="text-pink-8"
        >
          <q-item-section avatar>
            <q-icon name="help" size="md" color="pink-6" />
          </q-item-section>

          <q-item-section class="text-h6 text-weight-bold text-pink-9">About</q-item-section>
        </q-item>
      </q-list>

    </q-drawer>

    <q-drawer show-if-above v-model="right" side="right" bordered class="bg-pink-1">
      <q-input
        placeholder="Search Qwitter"
        class="q-ma-md"
        outlined
        rounded
        dense
        color="pink-6"
      >
        <template v-slot:prepend>
          <q-icon name="search" color="pink-5" />
        </template>
      </q-input>

      <q-list
        separator
        padding
      >
        <q-item class="q-pa-md">
          <q-item-section>
            <q-item-label overline class="text-pink-4">Education</q-item-label>
            <q-item-label class="text-weight-bold text-pink-9">Something amazing happened!</q-item-label>
            <q-item-label caption class="text-pink-7">Secondary line text. Lorem ipsum dolor sit amet, consectetur adipiscit elit.</q-item-label>
          </q-item-section>

          <q-item-section side top>
            <q-item-label caption class="text-pink-5">5 min ago</q-item-label>
          </q-item-section>
        </q-item>
        <q-item class="q-pa-md">
          <q-item-section>
            <q-item-label overline class="text-pink-4">Education</q-item-label>
            <q-item-label class="text-weight-bold text-pink-9">Something amazing happened!</q-item-label>
            <q-item-label caption class="text-pink-7">Secondary line text. Lorem ipsum dolor sit amet, consectetur adipiscit elit.</q-item-label>
          </q-item-section>

          <q-item-section side top>
            <q-item-label caption class="text-pink-5">5 min ago</q-item-label>
          </q-item-section>
        </q-item>
        <q-item class="q-pa-md">
          <q-item-section>
            <q-item-label overline class="text-pink-4">Education</q-item-label>
            <q-item-label class="text-weight-bold text-pink-9">Something amazing happened!</q-item-label>
            <q-item-label caption class="text-pink-7">Secondary line text. Lorem ipsum dolor sit amet, consectetur adipiscit elit.</q-item-label>
          </q-item-section>

          <q-item-section side top>
            <q-item-label caption class="text-pink-5">5 min ago</q-item-label>
          </q-item-section>
        </q-item>
      </q-list>
    </q-drawer>

    <q-page-container>
      <keep-alive>
        <router-view />
      </keep-alive>
    </q-page-container>

  </q-layout>
</template>

<script>
export default {
  data () {
    return {
      left: false,
      right: false
    }
  }
}
</script>

<style lang="sass">
.header-icon
  position: absolute
  bottom: 0
  left: 50%
  transform: translateX(-50%)
</style>
