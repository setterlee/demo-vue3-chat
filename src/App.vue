<template>
  <n-config-provider>
    <n-dialog-provider>
      <n-notification-provider
        ><n-layout>
          <n-layout-content>
            <n-message-provider :duration="6000" :placement="'bottom'">
              <router-view :key="route.fullPath" />
            </n-message-provider>
          </n-layout-content>
          <n-layout-footer> </n-layout-footer> </n-layout
      ></n-notification-provider>
    </n-dialog-provider>
  </n-config-provider>
</template>

<script>
import { useRoute } from "vue-router";
import {
  NConfigProvider,
  NNotificationProvider,
  NDialogProvider,
  NLayout,
  NLayoutContent,
  NMessageProvider,
  NLayoutFooter,
} from "naive-ui";

export default {
  components: {
    NConfigProvider,
    NNotificationProvider,
    NDialogProvider,
    NLayout,
    NLayoutContent,
    NMessageProvider,
    NLayoutFooter,
  },
  setup() {
    const route = useRoute();

    return {
      route,
    };
  },
};
</script>

<style lang="scss">
#app,
.n-drawer-container {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  max-width: 1500px;
  margin: 0 auto;
}
body {
  margin-bottom: 70px;
}
.n-layout-content {
  padding: 14px;
}
.n-layout .n-layout-scroll-container {
  overflow-x: unset;
  box-sizing: unset;
}
</style>
