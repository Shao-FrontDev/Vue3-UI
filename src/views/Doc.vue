<template>
  <div class="layout">
    <Topnav class="nav" />
    <div class="content">
      <aside v-if="menuVisible">
        <h4>COMPONENTS</h4>
        <ol>
          <li>
            <router-link to="/doc/switch"
              >Switch</router-link
            >
          </li>
          <li>
            <router-link to="/doc/button"
              >Button</router-link
            >
          </li>
          <li>
            <router-link to="/doc/dialog"
              >Dialog</router-link
            >
          </li>
          <li>
            <router-link to="/doc/tabs">Tabs</router-link>
          </li>
          <li>
            <router-link to="/doc/card">Card</router-link>
          </li>
        </ol>
      </aside>
      <main><router-view></router-view></main>
    </div>
  </div>
</template>

<script lang="ts">
import { inject, Ref } from "vue";
import Topnav from "../components/TopnavDemo.vue";
export default {
  components: {
    Topnav,
  },
  setup() {
    const menuVisible = inject<Ref<boolean>>("menuVisible");
    return {
      menuVisible,
    };
  },
};
</script>

<style lang="scss" scoped>
.layout {
  display: flex;
  flex-direction: column;
  height: 100vh;
  > .nav {
    flex-shrink: 0;
    
  }
  > .content {
    flex-grow: 1;
    padding-top: 60px;
    padding-left: 156px;
    @media (max-width: 500px) {
      padding-left: 0;
    }
  }
}
.content {
  display: flex;
  > aside {
    flex-shrink: 0;
    z-index: 1;
  }
  > main {
    flex-grow: 1;
    padding: 16px;
    background: white;
  }
}

aside {
  width: 150px;
  padding: 16px;
  position: fixed;
  top: 0;
  left: 0;
  padding-top: 70px;
  height: 100%;
  > h2 {
    margin-bottom: 4px;
  }
  > ol {
    > li {
      margin: 10px 0;
      padding: 4px 4px;
      text-align: center;
      &:hover {
        transition: all 1s ease;
        background: #333;
        text-transform: uppercase;
        color: white;
        border-radius: 5px;
      }
    }
  }
}
main {
  overflow: auto;
}
</style>
