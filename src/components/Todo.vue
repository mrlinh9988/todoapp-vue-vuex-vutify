<template>
  <div style="height: 100%">
    <v-container fluid fill-height pl-0 pr-0 pb-0 pt-0>
      <v-layout row align-space-between justify-sapce-between>
        <v-flex lg3 pr-2 pl-2>
          <list />
        </v-flex>

        <v-flex lg6 pr-2 pl-2>
          <!-- <Tasks /> -->
          <router-view name="tasks" :key="$route.fullPath"></router-view>
        </v-flex>

        <v-flex lg3 pl-2>
          <Optionbar />
          <router-view></router-view>
        </v-flex>
      </v-layout>
      <Notification />
    </v-container>
  </div>
</template>

<script>
import List from "@/components/List";
import Notification from "@/components/Notification";
// import Tasks from "@/components/Tasks";
import Optionbar from "@/components/Optionbar";

export default {
  name: "todo",
  components: {
    List,
    // Tasks,
    Optionbar,
    Notification,
  },
};
</script>

<style>
</style>