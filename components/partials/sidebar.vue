<template>
  <div class="main-sidebar">
    <aside id="sidebar-wrapper">
      <div class="sidebar-brand">
        <a href="index.html">Stisla</a>
      </div>
      <div class="sidebar-brand sidebar-brand-sm">
        <a href="index.html">St</a>
      </div>
      <ul class="sidebar-menu">
        <li v-for="(menu, i) in listMenu" :key="i">
          <nuxt-link class="nav-link" :to="menu.to">
            <i :class="menu.icon"></i> <span>{{ menu.name }} </span>
          </nuxt-link>
        </li>
        <!-- <li v-for="(item,i) in listClass" :key="i">
          <nuxt-link class="nav-link" to="/example/http-request/">
            <i class="far fa-bookmark"></i> <span>{{item.name}} </span>
          </nuxt-link>
        </li> -->
      </ul>
    </aside>
  </div>
</template>

<script>
export default {
  data() {
    return {
      listMenu: [
        {
          name: "Semua Kelas",
          icon: "fas fa-home",
          to: "/"
        }
      ]
    };
  }
};
</script>
