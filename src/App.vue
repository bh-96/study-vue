<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <v-app-bar-nav-icon @click="drawer = !drawer" />

      <v-spacer />
    </v-app-bar>
    <!-- app: 기본 레이아웃 컴포넌트로 만들어주는 특수 속성 -->
    <v-navigation-drawer
      v-model="drawer"
      app
      :src="require('@/assets/sidebar.jpg')"
      dark
    >
      <template
        v-slot:img="props"
      >
        <v-img
          :gradient="gradient"
          v-bind="props"
        />
      </template>
      <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="text-h6">
            Application
          </v-list-item-title>
          <v-list-item-subtitle>
            subtext
          </v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-divider />

      <v-list
        dense
        nav
      >
        <v-list-item
          v-for="item in items"
          :key="item.title"
          link
          :to="item.to"
          active-class="primary"
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-main>
      <v-container>
        <router-view />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    drawer: false,
    gradient: 'rgba(0, 0, 0, .7), rgba(0, 0, 0, .7)',
    items: [
      { title: 'Dashboard', icon: 'mdi-view-dashboard', to: '/' },
      { title: 'GridSystem', icon: 'mdi-view-dashboard', to: '/grid-system' },
      { title: 'GridListPage', icon: 'mdi-view-dashboard', to: '/grid-list-page' },
      { title: 'Breakpoints', icon: 'mdi-view-dashboard', to: '/breakpoints' },
      { title: 'Typography', icon: 'mdi-view-dashboard', to: '/typography' },
      { title: 'Tables', icon: 'mdi-view-dashboard', to: '/tables' },
      { title: 'Forms', icon: 'mdi-view-dashboard', to: '/forms' },
      { title: 'Icons', icon: 'mdi-view-dashboard', to: '/icons' },
      { title: 'Buttons', icon: 'mdi-view-dashboard', to: '/buttons' },
    ],
    right: null,
  }),
};
</script>
